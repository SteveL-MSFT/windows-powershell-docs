---
author: brianlic-msft-msft
description: 
external help file: Microsoft.IdentityServer.Management.dll-Help.xml
keywords: powershell, cmdlet
manager: alanth
ms.date: 2016-12-20
ms.prod: powershell
ms.technology: powershell
ms.topic: reference
online version: 
schema: 2.0.0
title: Revoke-AdfsApplicationPermission
ms.assetid: F92E53E3-E17D-4C78-ABA7-E0E66BBA25F0
---

# Revoke-AdfsApplicationPermission

## SYNOPSIS
Revokes permission for an application.

## SYNTAX

### Identifier (Default)
```
Revoke-AdfsApplicationPermission [-TargetIdentifier] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RoleIdentifier
```
Revoke-AdfsApplicationPermission [[-TargetClientRoleIdentifier] <String>]
 [[-TargetServerRoleIdentifier] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Revoke-AdfsApplicationPermission [-InputObject] <OAuthPermission> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Revoke-AdfsApplicationPermission** cmdlet revokes permission for an application in Active Directory Federation Services (AD FS).

## EXAMPLES

### 1:
```

```

## PARAMETERS

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

### -InputObject
Specifies an **OAuthPermission** object.

```yaml
Type: OAuthPermission
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TargetClientRoleIdentifier
Speci

```yaml
Type: String
Parameter Sets: RoleIdentifier
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -TargetIdentifier


```yaml
Type: String
Parameter Sets: Identifier
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetServerRoleIdentifier


```yaml
Type: String
Parameter Sets: RoleIdentifier
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AdfsApplicationPermission](./Get-AdfsApplicationPermission.md)

[Grant-AdfsApplicationPermission](./Grant-AdfsApplicationPermission.md)

[Set-AdfsApplicationPermission](./Set-AdfsApplicationPermission.md)
