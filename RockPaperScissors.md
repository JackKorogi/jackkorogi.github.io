```mermaid
%%{init: {'themeVariables': { 'nodeSpacing': '250', 'rankSpacing': '250'}}}%%
flowchart TD

A[Start Game] --> B{Player Chooses}
B --> C[Rock]
B --> D[Paper]
B --> E[Scissors]

C --> F[Computer picks Rock]
C --> G[Computer picks Paper]
C --> H[Computer picks Scissors]

D --> I[Computer picks Rock]
D --> J[Computer picks Paper]
D --> K[Computer picks Scissors]

E --> L[Computer picks Rock]
E --> M[Computer picks Paper]
E --> N[Computer picks Scissors]

F --> O(Game is a tie)
J --> O
N --> O
G --> P(Game is a loss)
K --> P
L --> P
H --> Q(Game is a win)
I --> Q
M --> Q

O --> R{END}
P --> R
Q --> R
```
1. B --> C, D, E
   - ***C**, **D**, and **E** are the three different choices the player can pick (rock, paper, and scissors, respectively.*
2. C --> F, G, H; D --> I, J, K; E --> L, M, N
   - *These all represent rock, paper, and scissors respectively connecting to the computer picks for rock, paper, and scissors respectively*
3. F, J, N --> O; G, K, L --> P; H, I, M --> Q
   - *This connects the tie, loss, and win conditions to the choices that result in either a tie, win, or loss.*
