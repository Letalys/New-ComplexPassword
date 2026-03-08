
# New-ComplewPassword

This is my own reusable and easily configurable password generator.

I hope you enjoy it  ;)

## Using Module [New-ComplexPassword.psm1](./New-ComplexPassword.psm1)

If you are only interested in the function module to integrate in you own app, you just have to get it from the "lib" directory

### How to use

You can save the PSM1 file wherever you want. Then simply import it directly into your code, specifying its location.

`Import-Module "New-ComplexPassword.psm1" -Force`

Next you just have to specify your call parameters.

The NoRepeat option is used to generate a password with no duplicate characters. However if the unique character set available according to the options is less than the MinimumLenght option, the password will ignore this parameter.

_Example :_
```
$PasswordParameters = @{
        MinimumLength = 12
        IncludeUppercase = $true
        IncludeLowercase = $true
        IncludeNumbers =  $true
        IncludeSymbols = $true
        IncludeOtherSymbols = $true
        NoRepeat = $true
    }

    $result = Get-RandomPassword @PasswordParameters

    Write-Host $result.Password
    Write-Host = $result.Strength
```

```
New-ComplexPassword -MinimumLength 12 -IncludeUppercase $true -IncludeLowercase $true -IncludeNumbers $false - IncludeSymbols $true -IncludeOtherSymbols $false -NoRepeat $false
```

## Autor
- [@Letalys (GitHUb)](https://www.github.com/Letalys)
