# mkSecrets

A bash script to create a source-able secrets file using a secrets-template for your project.  
mkSecrets takes also care of your .gitignore definition related to the .secrets file.

## Usage

```none
-t <templateFile>  Use a template for secrets fron given path [default: ./secrets.tmpl]"
-o <outputPath>    Save the secrets-file .secrets in given path [default: ./.secrets]"
-n                 no .gitignore setup [default: set .secrets in .gitignore]"
-h, ?              Display the help message"
```

## Template

The template is structured with an associative array.  
The struct is variablename to variable descrition.  
Using ';insecure' at the end of the description line will prevent hiding keystrokes during input!

### Template example

```bash
declare -A secrets=(
    [uiPassword]="This Password is used to set the Admin account"
    [appToken]="Enter the API-Token;insecure"
)
```
