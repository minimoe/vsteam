<!-- #include "./common/header.md" -->

# Add-VSTeamProfile

## SYNOPSIS

<!-- #include "./synopsis/Add-VSTeamProfile.md" -->

## SYNTAX

## DESCRIPTION

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------

```PowerShell
PS C:\> Add-VSTeamProfile
```

You will be prompted for the account name and personal access token.

### -------------------------- EXAMPLE 2 --------------------------

```PowerShell
PS C:\> Add-VSTeamProfile -Account mydemos -PersonalAccessToken 7a8ilh6db4aforlrnrqmdrxdztkjvcc4uhlh5vgbteserp3mziwnga -Version TFS2018
```

Allows you to provide all the information on the command line.

### -------------------------- EXAMPLE 3 --------------------------

```PowerShell
PS C:\> Add-VSTeamProfile -Account http://localtfs:8080/tfs/DefaultCollection -UseWindowsAuthentication
```

On Windows, allows you use to use Windows authentication against a local TFS server.

## PARAMETERS

### -Account

The Visual Studio Team Services (VSTS) account name to use.
DO NOT enter the entire URL.

Just the portion after dev.azure.com. For example in the
following url mydemos is the account name.
<https://dev.azure.com/mydemos>
or
The full Team Foundation Server (TFS) url including the collection.
<http://localhost:8080/tfs/DefaultCollection>

```yaml
Type: String
Parameter Sets: Secure, Plain, Windows
Required: True
Position: 1
```

### -PAT

A secured string to capture your personal access token.

This will allow you to provide your personal access token
without displaying it in plain text.

To use pat simply omit it from the Add-VSTeamProfile command.

```yaml
Type: SecureString
Parameter Sets: Secure
Required: True
```

### -PersonalAccessToken

The personal access token from VSTS/TFS to use to access this account.

```yaml
Type: String
Parameter Sets: Plain
Required: True
Position: 2
```

### -UseWindowsAuthentication

Allows the use of the current user's Windows credentials to authenticate against a local TFS.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
```

### -UseBearerToken

Switches the authorzation from Basic to Bearer.  You still use the PAT for PersonalAccessToken parameters to store the token.

```yaml
Type: SwitchParameter
Parameter Sets: Secure, Plain
```

### -Name

Optional name for the profile. If this parameter is not provided the account will also serve as the name.

```yaml
Type: String
Required: True
Position: 3
```

<!-- #include "./params/version.md" -->

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-VSTeamAccount](Set-VSTeamAccount.md)

[Set-VSTeamDefaultProject](Set-VSTeamDefaultProject.md)