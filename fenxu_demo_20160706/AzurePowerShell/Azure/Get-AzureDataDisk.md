---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureDataDisk
## SYNOPSIS
Gets Azure data disks.

## SYNTAX

```
Get-AzureDataDisk [[-Lun] <Int32>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>]
```

## DESCRIPTION
The Get-AzureDataDisk cmdlet gets an object that represents the data disks on an Azure virtual machine.
To get a specific data disk object, specify the logical unit number (LUN) of the disk.

## EXAMPLES

### --------------------------  Example 1: Get all data disks for a virtual machine  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk
```

This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the Get-AzureVM cmdlet.
The command passes the virtual machine to the current cmdlet by using the pipeline operator.
The current cmdlet gets all the data disks for this virtual machine.

### --------------------------  Example 2: Get a specific data disk for a vitural machine  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk -LUN 2
```

This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.
The command passes the virtual machine to the current cmdlet.
The current cmdlet gets the data disk that has the LUN 2.

## PARAMETERS

### -Lun
Specifies the LUN for the data drive in the virtual machine.
Valid values are: 0 through 15.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Specifies the virtual machine object for which this cmdlet gets data disks.
To obtain a virtual machine object, use the Get-AzureVM cmdlet.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

## NOTES

## RELATED LINKS

[Add-AzureDataDisk]()

[Get-AzureVM]()

[Remove-AzureDataDisk]()

[Set-AzureDataDisk]()

