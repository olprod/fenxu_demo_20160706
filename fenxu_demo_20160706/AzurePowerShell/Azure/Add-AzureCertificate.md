---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
online version: 
schema: 2.0.0
---

# Add-AzureCertificate
## SYNOPSIS
Uploads a certificate to an Azure cloud service.

## SYNTAX

```
Add-AzureCertificate [-ServiceName] <String> [-CertToDeploy] <Object> [-Password <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
```

## DESCRIPTION
The Add-AzureCertificate cmdlet uploads a certificate for an Azure service.

## EXAMPLES

### --------------------------  Example 1: Upload a certificate and password  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy ContosoCertificate.pfx -Password "password"
```

This command uploads the certificate file ContosoCertificate.pfx to a cloud service.
The command specifies the password for the certificate.

### --------------------------  Example 2: Upload a certificate file  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Add-AzureCertificate -serviceName "MyService" -CertToDeploy ContosoCertificate.cer
```

This command uploads the certificate file ContosoCertificate.cer to a cloud service.
The command specifies the password for the certificate.

### --------------------------  Example 3: Upload a certificate object  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>$Certificate = Get-Item cert:\PATTIFULLER\MY\1D6E34B526723E06C235BE8E5457784BF12C9F39
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy $Certificate
```

The first command gets a certificate from the MY store of a user by using the Windows PowerShell core Get-Item cmdlet.
The command stores the certificate in the $Certificate variable.

## PARAMETERS

### -ServiceName
Specifies the name of the Azure service to which this cmdlet adds a certificate.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertToDeploy
Specifies the certificate to deploy.
You can specify the full path of a certificate file, such as a file that has a *.cer or *.
pfx file name extension, or an X.509 Certificate object.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
Specifies the certificate password.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Specifies the Azure profile from which this cmdlet reads.
If you do not specify a profile, this cmdlet reads from the local default profile.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
@{Text=}

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: 
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
@{Text=}

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: 
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

### ManagementOperationContext

## NOTES

## RELATED LINKS

[Get-AzureCertificate]()

[New-AzureCertificateSetting]()

[Remove-AzureCertificate]()

