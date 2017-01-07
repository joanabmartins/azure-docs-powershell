---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 58B7F92C-DB2A-4544-941C-4852A59C7982
---

# Remove-AzureAclConfig

## SYNOPSIS
Removes an ACL configuration object from an Azure virtual machine configuration.

## SYNTAX

```
Remove-AzureAclConfig [-EndpointName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureAclConfig** cmdlet removes an access control list (ACL) configuration object from an Azure virtual machine configuration.

## EXAMPLES

### Example 1: Remove an ACL configuration
```
PS C:\>Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureAclConfig -EndpointName "Web" | Update-AzureVM
```

This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the Get-AzureVM cmdlet.
The command passes that object to the current cmdlet by using the pipeline operator.
That cmdlet removes the ACL configuration for the endpoint named Web.
The command passes the result to the Update-AzureVM cmdlet, which updates the virtual machine.

## PARAMETERS

### -EndpointName
Specifies the name of the endpoint from which this cmdlet removes the ACL configuration.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Specifies the virtual machine from which this cmdlet removes an ACL configuration.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureAclConfig](./Get-AzureAclConfig.md)

[Get-AzureVM](./Get-AzureVM.md)

[New-AzureAclConfig](./New-AzureAclConfig.md)

[Set-AzureAclConfig](./Set-AzureAclConfig.md)

[Update-AzureVM](./Update-AzureVM.md)

