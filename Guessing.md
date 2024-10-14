``` mermaid
    flowchart TD;
    ShowStart([Start]) --> Start[/Get User Input/]
    Start --> CheckIfValid[Checks If Input Is A Valid Number]
    CheckIfValid -- Is NOT A Valid Number --> ShowStart
    CheckIfValid -- Is A Valid Number --> CheckIfCorrect{Check If Inputed Number Is Less Than, Greater Than, Or Equal To The Number}
    CheckIfCorrect -- Inputed Number < Number --> OutputLow[/"Number Is Too Low"/]
    OutputLow --> Start
    CheckIfCorrect -- Inputed Number > Number --> OutputHigh[/"Number Is Too High"/]
    OutputHigh --> Start
    CheckIfCorrect -- Inputed Number = Number --> OutputWin[/Outputs "You Guessed The Correct Number"/]
    OutputWin --> ShowEnd([End])
```

#### ShowStart - Shows the start
#### Start - Gets User Input
#### CheckIfValid - Checks If User Input Is A Valid Number
#### CheckIfCorrect - Checks If User Input Is Less Than, Greater Than, Or Equal To The Number
#### ShowEnd - Shows the end