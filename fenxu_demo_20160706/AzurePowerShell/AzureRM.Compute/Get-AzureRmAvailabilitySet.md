---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureRmAvailabilitySet
## SYNOPSIS
Gets Azure availability sets in a resource group.

## SYNTAX

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>]
```

## DESCRIPTION
The Get-AzureRmAvailabilitySet cmdlet gets Azure availability sets in a resource group.
You can specify the name of a specific availability set to get.

## EXAMPLES

### --------------------------  Example 1: Get a specific availability set  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.

### --------------------------  Example 2: Get all availability sets  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

This command gets all the availability sets in the resource group named ResourceGroup11.

## PARAMETERS

### -ResourceGroupName
Specifies the name of a resource group.

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

### -Name
Specifies the name of an availability set that this cmdlet gets.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[New-AzureRmAvailabilitySet]()

[Remove-AzureRmAvailabilitySet]()

