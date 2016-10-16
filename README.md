# Closure-Set
> Finds all closures for a given keyset [**WINDOWS Only**]

## Usage
>
- Open Powershell [*With Admin, if you don't have ExecutionPolicy enabled*]
- If your *execution policy* is not correct, or you have no idea what I'm saying:
  - In your shell enter `Set-ExecutionPolicy RemoteSigned`
  - This allows script to be allowed to run in your PowerShell console
- Cd to the directory where this script is downloaded
- Copy the rule to your clipboard (the script will read the rules from there!)
  - If this isn't done, the script will also ask you for the ruleset on execution
- run `./Closure-Set.ps1`

## Examples
>
- Normal Example [Copy the rules to your clipboard first]:
 - Copied my rules [`AB → C, CD → E, EF → G, FG → E, DE → C, and BC → A`]
 - run `./Closure-Set.ps1`
 - Output:
 ```powershell
 [+] Rules:
    [+] AB -> C
    [+] CD -> E
    [+] EF -> G
    [+] FG -> E
    [+] DE -> C
    [+] BC -> A
Enter Query: ABD
ABCDE
Enter Query: 
 ```
- With Mask [Copy the rules to your clipboard first]:
 - Copied my rules [`AB → C, CD → E, EF → G, FG → E, DE → C, and BC → A`]
 - run `./Closure-Set.ps1 -Mask`
 - Output:
 ```powershell
 [+] Rules:
    [+] AB -> C
    [+] CD -> E
    [+] EF -> G
    [+] FG -> E
    [+] DE -> C
    [+] BC -> A
Enter Query: ABD
CE
Enter Query: 
 ```

## Parameters
> 
param | Definition
----- | ----------
-Mask | Only show added characters from the traversal
