# PlayLive 2.3.0 — Manual do Usuário

**PlayLive Player** — controle de reprodução de áudio ao vivo por teclado e MIDI.

---

## 1. O que é o PlayLive

O PlayLive é um **player de áudio para uso ao vivo**, controlado por teclado ou por
controlador MIDI. Ele foi feito para a mão ficar no teclado durante a performance:
você atribui uma tecla ou um controle MIDI a cada faixa, e dispara tudo sem tirar
os olhos do palco.

- **20 pads** por aba, **2 abas** (Aba A e Aba B) = **40 slots** no total.
- Cada aba toca **independentemente**: cada uma tem seu próprio volume, botão STOP
  e tempo restante. É possível ter música tocando na Aba A enquanto a Aba B toca
  outra coisa.
- **Sem limites** de tempo, de faixas ou de pads: todos os 40 slots ficam
  disponíveis desde o primeiro uso.

> O PlayLive **não captura áudio do microfone** e não faz gravação. Ele apenas
> reproduz os arquivos de áudio que você atribuir.

---

## 2. Requisitos

| Item | Requisito |
|---|---|
| Sistema | Windows 10 versão 1809 ou superior, ou Windows 11 |
| Arquitetura | 64 bits (x64) |
| Memória | 2 GB livres |
| Áudio | Qualquer dispositivo de saída suportado pelo Windows |
| MIDI | Opcional — apenas um controlador compatível com MIDI já conectado |
| Rede | Necessária apenas para instalar, ativar a licença e comprar |

---

## 3. Instalação

1. Abra a **Microsoft Store** e localize **PlayLive** (pesquis pelo nome do
   desenvolvedor, *Jantonybit*).
2. Clique em **Obter** ou **Instalar**.
3. O PlayLive é publicado pela Microsoft Store. O Windows exibe o selo de
   **editor verificado** e o app é assinado digitalmente pela Microsoft.

O PlayLive **não** é distribuído como instalador `.exe` avulso. Se você encontrar
um arquivo `.msix` na internet, ele não veio do canal oficial.

### Licença e teste de 30 dias

Na primeira abertura, o PlayLive oferece um **teste gratuito de 30 dias**, com
todas as funções liberadas — não existe versão reduzida.

- O app verifica a licença a cada poucos segundos e mostra um aviso na parte de
  cima quando restam **5 dias** ou menos.
- Ao terminar o teste, o app entra em modo bloqueado e oferece o botão
  **Comprar na Microsoft Store**.
- A compra é vitalícia: você paga **uma vez** e o app fica desbloqueado para
  sempre, sem assinatura e sem cobrança recorrente.
- Depois da compra, basta reabrir o PlayLive. O desbloqueio é feito
  automaticamente.

---

## 4. Conhecendo a tela

```
┌──────────────────────────────────────────────────────────────────┐
│  PlayLive                                      [⚙ Configurações] │  ← cabeçalho
├──────────────────────────────────────────────────────────────────┤
│  Volume  ──────────────────●──────────────────────                │
│  Aba A ●──────── Balance entre Abas ────────────●──── Aba B     │
├──────────────────────────────────────────────────────────────────┤
│                          [ Aba A ] [ Aba B ]                      │  ← abas
│  ┌────┐  ┌────┐  ┌────┐  ┌────┐  ┌────┐                          │
│  │Slot│  │Slot│  │Slot│  │Slot│  │Slot│                          │
│  │  1 │  │  2 │  │  3 │  │  4 │  │  5 │                          │
│  └────┘  └────┘  └────┘  └────┘  └────┘                          │
│   ...     ...     ...     ...     ...      (4 linhas × 5)        │
│                                                                  │
│  ┌───────────────┐  ┌──────────────────┐                         │
│  │ ⏹ STOP - Aba A│  │ Tempo Restante   │                         │
│  └───────────────┘  │      04:32       │                         │
├──────────────────────────────────────────────────────────────────┤
│  [ VU / nível de áudio ]                                        │
└──────────────────────────────────────────────────────────────────┘
```

### Pads

Cada pad mostra:

- o **nome do arquivo** atribuído (ou `Slot N` se estiver vazio);
- no canto superior esquerdo, a **próxima ação** configurada para quando a faixa
  terminar;
- no canto inferior direito, a **duração da faixa**;
- uma **barra de progresso** durante a reprodução;
- **verde** quando está tocando, **azul** quando está selecionado pela
  navegação, e a cor que você atribuiu quando está ocioso.

### Botão STOP

Um botão STOP por aba. Ele para **somente a aba correspondente** — a outra aba
continua tocando normalmente. Também é possível configurar um *fade-out* para
que a música não termine de forma abrupta.

### Volume e Balance

- **Volume** controla o volume geral do app (0 a 100).
- **Balance entre Abas** decide qual aba domina a mixagem. Totalmente à
  esquerda, a Aba A fica no volume máximo e a Aba B é silenciada; totalmente à
  direita, o inverso. No centro, as duas tocam juntas com o mesmo peso.

Isso permite passar de uma música para outra com um fade natural, sem cortar
nada abruptamente.

### Tempo Restante

Contador regressivo da faixa em reprodução na aba atual, no formato `MM:SS`.

---

## 5. Controle por teclado

O teclado é o controle principal. **O botão esquerdo do mouse não dispara as
faixas** — isso é intencional, para que uma depuração acidental no palco não
dispare o áudio.

### Navegação

| Tecla | Ação |
|---|---|
| `←` `→` | Move a seleção para o pad ao lado |
| `↑` `↓` | Move a seleção 5 pads (uma linha) |
| `Enter` | Toca o pad selecionado |
| `Tab` | Alterna entre a Aba A e a Aba B |
| `Espaço` | Para a aba atual (equivalente ao botão STOP) |
| `F11` | Entra e sai da tela cheia |

Segurar uma seta faz a seleção se mover em sequência (após 350 ms, repetindo a
cada 80 ms), o que permite atravessar a grade rapidamente.

### Atribuir teclas às faixas

Cada um dos 40 slots pode receber uma tecla. Para mapear:

1. **Clique com o botão direito** no pad desejado.
2. Escolha **⌨ Teclado**.
3. Clique em **Mapear Tecla do Teclado** (ou **Capturar Nova Tecla**).
4. Pressione a tecla que deseja usar.
5. Confirme com **Confirmar**.

Uma tecla fica associada a **um único slot por aba**. Se você mapear uma tecla que
já está em uso, ela é transferida para o novo slot — o mapeamento anterior é
descartado silenciosamente. Para evitar carotenha, confira a lista de teclas
antes de mexer em um set que já funciona.

É possível adicionar teclas extras ao mesmo slot (cada slot aceita várias
teclas) e removê-las pelos botões `✖` ao lado da lista.

---

## 6. Controle por MIDI

Conecte o controlador MIDI **antes** de abrir o PlayLive. O app detecta os
dispositivos automaticamente ao iniciar.

Para mapear qualquer controle, o procedimento é o mesmo nos três casos:

1. Abra a janela de configuração desejada.
2. Clique em **🎹 MIDI Learn**.
3. Mova o controle físico (botão, pedal, fader, knob) no seu controlador.
4. O app captura o controle e exibe o nome detectado.

### O que pode ser mapeado

| Controle | Onde configurar |
|---|---|
| Tocar um slot | Configuração do pad (clique direito no pad) |
| Parar a aba | **⏹ STOP** → `MIDI Learn Stop` |
| Alternar abas | **Alternância de Abas** → `MIDI Learn Trocar Aba` |
| Volume geral | **Configurações do Volume** → `MIDI Learn Volume` |
| Balance entre abas | **Configurações do Balance** → `MIDI Learn Balance` |

> O mapeamento é salvo junto com a cena. Ao trocar de cena, o mapeamento MIDI
> também troca.

---

## 7. Configurando um pad

**Clique com o botão direito** no pad:

| Item | O que faz |
|---|---|
| **Arquivo / Selecionar Música** | Escolhe o arquivo de áudio do slot |
| **🎹 MIDI Learn** | Associa um controle MIDI a este slot |
| **⌨ Teclado** | Associa uma tecla a este slot |
| **Ação após terminar** | Define o que acontece quando a faixa acaba (ver abaixo) |
| **🎨 Escolher Cor** | Altera a cor do pad |
| **Resetar Configurações do Botão** | Volta o slot ao estado padrão |
| **Salvar e Fechar** | Grava e fecha a janela |
| **Fechar sem salvar** | Descarta as alterações desta janela |

### Ação após terminar

Quando a faixa chega ao fim, o slot pode:

- **Parar** — a reprodução é encerrada (padrão);
- **Loop** — a faixa recomeça do início indefinidamente;
- **Próximo** — o app avança para a próxima faixa da pasta;
- **Selecionar** — dispara outro slot específico. Use **Selecionar Destino** para
  escolher a aba e o botão de destino. Esta opção cria um encadeamento: ao final
  de uma faixa, a próxima começa sozinha.

> **Loop** é ideal para a base instrumental de uma apresentação. **Selecionar**
> permite montar uma sequência inteira sem tocar em nada.

---

## 8. Configurando o STOP

**Clique com o botão direito** no botão STOP da aba desejada:

- **🎹 MIDI Learn Stop** — mapeia um controle MIDI para parar a aba;
- **Fadeout ao Parar** — de **0 ms (corte)** a **3000 ms**. Em 0 o áudio é
  interrompido imediatamente; em 3000 ms o volume cai suavemente ao longo de
  3 segundos;
- **Crossfade ao Trocar Faixa** — quando ativado, a faixa que está saindo recebe
  o mesmo *fade-out* do STOP enquanto a próxima entra. Ideal para sequências
  seguidas.

> O crossfade usa a mesma duração definida no *fade-out*. Ajuste a duração acima
> para controlar a transição.

---

## 9. Configurações do Volume e do Balance

**Clique com o botão direito** no slider correspondente:

- **Volume** — `MIDI Learn Volume`, e o ajuste fino do volume geral;
- **Balance** — `MIDI Learn Balance`, e o ajuste do equilíbrio entre as abas.

Os dois sliders respondem tanto ao mouse quanto ao MIDI.

---

## 10. Alternância de abas

**Clique com o botão direito** no cabeçalho das abas:

- **Mapeamento de Troca de Aba** — define a tecla que alterna entre as abas;
- **🎹 MIDI Learn Trocar Aba** — mapeia um controle MIDI.

O `Tab` já funciona de fábrica, independentemente dessa configuração. O mapeamento
adicional serve para Scratch, pedal ou botão dedicado.

---

## 11. Cenas

Uma **cena** guarda todo o estado do app: faixas de cada slot, cores, mapeamentos
de teclado e MIDI, volume, balance e parâmetros de fade.

Para abrir as opções de cena, clique no botão **⚙** no canto superior direito:

| Botão | Ação |
|---|---|
| **Salvar Cena** | Grava a configuração atual em arquivo |
| **Importar Cena** | Carrega uma cena salva |
| **🔴 RESETAR TODAS AS CONFIGURAÇÕES** | Apaga tudo e volta ao padrão |

> ⚠️ **Esta ação não pode ser desfeita.** O botão fica dentro da **ZONA DE PERIGO**
> e pede confirmação.

O PlayLive também guarda automaticamente a **última cena usada** e a recarrega na
próxima abertura, para você retomar de onde parou.

---

## 12. Tela cheia

Pressione `F11` (ou `F11` novamente para sair). É o modo recomendado para uso ao
vivo, já que esconde a barra de tarefas e as distrações da tela.

Para sair da tela cheia por outros meios, use `Alt+Tab` para chamar o gerenciador
de tarefas e selecione `Esc` na sobreposição do Windows.

---

## 13. Solução de problemas

**Não consigo carregar um arquivo.**
Verifique se o arquivo não está aberto em outro programa que o bloqueie. O
PlayLive toca os formatos suportados pelo sistema — de Preference, **WAV** e
**MP3** são os mais confiáveis. Formatos comprimidos exóticos podem não ser
suportados pelo dispositivo de saída.

**O som sai por um lado só.**
Ajuste o **Balance entre Abas** para o centro. Verifique também o balance do
sistema operacional (Configurações de som do Windows).

**Nenhum controle MIDI é detectado.**
Feche e reabra o PlayLive depois de conectar o controlador. Se usar um hub USB,
tente conectar diretamente à porta. O cabo do controlador precisa ser MIDI, e
não apenas USB genérico.

**A tecla atribuída não dispara a faixa.**
Confirme que a focus está na janela do PlayLive. Se outra janela estiver em
primeiro plano, a tecla vai para ela. Também verifique se a mesma tecla não foi
reatribuída a outro slot.

**O aviso de teste continua aparecendo.**
A licença é revalidada automaticamente. Se o app foi movido de pasta ou o
Windows trocou de conta, feche completamente o PlayLive e abra novamente.

**O app está bloqueado pedindo a compra.**
Isso significa que o teste de 30 dias foi concluído (ou que esta cópia não veio
de um canal licenciado). Compre uma vez na Microsoft Store; o desbloqueio
acontece automaticamente na próxima abertura.

---

## 14. Atalhos de referência rápida

| Tecla | Ação |
|---|---|
| `F11` | Tela cheia |
| `Tab` | Alternar Aba A / Aba B |
| `←` `→` | Selecionar pad vizinho |
| `↑` `↓` | Selecionar linha acima / abaixo |
| `Enter` | Tocar pad selecionado |
| `Espaço` | Parar a aba atual |
| `Clique direito` | Configurar (pad, STOP, volume, balance, abas) |
| `Botão ⚙` | Cenas e reset |

---

*PlayLive 2.3.0 — Developed by Joao Antonio Gomes De Sa (Jantonybit)*
