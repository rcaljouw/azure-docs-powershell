---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 3F883CDC-D030-41F3-BF83-991AD57AA777
---

# Get-AzureRmApiManagementPolicy

## SYNOPSIS
Gets the specified scope policy.

## SYNTAX

### Tenant level (Default)
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Product level
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Operation level
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### API level
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.

## EXAMPLES

### Example 1: Get the tenant level policy
```
PS C:\> Get-AzureRmApiManagementPolicy -Context $APImContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

This command gets tenant level policy and saves it to a file named tenantpolicy.xml.

### Example 2: Get the product-scope policy
```
PS C:\> Get-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

This command gets product-scope policy

### Example 3: Get the API-scope policy
```
PS C:\> Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

This command gets API-scope policy.

### Example 4: Get the operation-scope policy
```
PS C:\> Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

This command gets the operation-scope policy.

## PARAMETERS

### -Context
Specifies an instance of **PsApiManagementContext**.

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Format
Specifies the format of the API management policy.
The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SaveAs
Specifies the file path to save the result to.
If you do not specify this parameter the result is pipelined as a sting.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProductId
Specifies the identifier of an existing product.
If you specify this parameter the cmdlet returns the product-scope policy.

```yaml
Type: String
Parameter Sets: Product level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApiId
Specifies the identifier of the existing API.
If you specify this parameter the cmdlet returns the API-scope policy.

```yaml
Type: String
Parameter Sets: Operation level, API level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OperationId
Specifies the identifier of the existing API operation.
If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.

```yaml
Type: String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### String

## NOTES

## RELATED LINKS

[Remove-AzureRmApiManagementPolicy](./Remove-AzureRmApiManagementPolicy.md)

[Set-AzureRmApiManagementPolicy](./Set-AzureRmApiManagementPolicy.md)


