---
author: brianlic-msft
description: 
external help file: FSRMClassification.cdxml-help.xml
keywords: powershell, cmdlet
manager: alanth
ms.date: 2016-12-20
ms.prod: powershell
ms.technology: powershell
ms.topic: reference
online version: 
schema: 2.0.0
title: Set-FsrmClassification
ms.assetid: 93C1EC77-FD4C-405B-9F33-644DBCF8A70C
---

# Set-FsrmClassification

## SYNOPSIS
Changes configuration settings for classification.

## SYNTAX

```
Set-FsrmClassification [-InputObject <CimInstance[]>] [-ExcludeNamespace <String[]>] [-Schedule <CimInstance>]
 [-Continuous] [-ContinuousLog] [-ContinuousLogSize <UInt64>] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-FsrmClassification** cmdlet changes configuration settings for classification.

## EXAMPLES

### Example 1: Set classification to run continuously
```
PS C:\>Set-FsrmClassification -Continuous -ContinuousLog
```

This command sets classification to run continuously and enables the continuous classification log.
If you have not previously created a classification schedule, the command results in an error.

### Example 2: Set the schedule for classification
```
The first command gets a **DateTime** object and stores it in the variable $D.
PS C:\>$D = Get-Date "12:00am"

The second command creates a **FsrmScheduledTask** object that defines a schedule for the task of once a month on the first day of the month at midnight. The command stores the **FsrmScheduledTask** object in the $Task variable.
PS C:\>$Task = New-FsrmScheduledTask -Time $D.ToFileTimeUtc() -Monthly 1

The third command sets the schedule for classification to the schedule stored in the $Task variable.
PS C:\>Set-FsrmClassification -Schedule $Task
```

This example sets the schedule for classification to run once a month on the first day at midnight.

## PARAMETERS

### -AsJob
{{Fill AsJob Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CimSession
Runs the cmdlet in a remote session or on a remote computer.
Enter a computer name or a session object, such as the output of a New-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227967 or Get-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227966 cmdlet.
The default is the current session on the local computer.

```yaml
Type: CimSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: Named
Default value: None
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

### -Continuous
Indicates that the server continuously applies classification to files in the background.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinuousLog
Indicates that the server maintains a log of continuous classification activities.
You must specify the *Continuous* parameter to log classification activities.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinuousLogSize
Specifies the maximum size of the log that contains continuous classification activity.
You must specify the *Continuous* parameter to log classification activities.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeNamespace
Specifies an array of strings that contain the list of folders to not include in classification (scheduled or continuous).

You can include \[AllVolumes\] in each folder at the start of a path to indicate that the namespace is excluded on all volumes.
You can append the string /s to each namespace to exclude all folders and files in that namespace.
If /s is not appended to the namespace, only the files in the specified folder are excluded.
If one string is \[Default\], the server adds the default values to the exclude namespaces.
The boot volume is always excluded regardless of this value.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
{{Fill InputObject Description}}

```yaml
Type: CimInstance[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
Specifies a File Server Resource Manager (FSRM) scheduled task object that describes the schedule for performing the continuous classification.
Use the New-FsrmScheduledTask cmdlet to create a scheduled task object.

```yaml
Type: CimInstance
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottleLimit
Specifies the maximum number of concurrent operations that can be established to run the cmdlet.
If this parameter is omitted or a value of `0` is entered, then Windows PowerShell® calculates an optimum throttle limit for the cmdlet based on the number of CIM cmdlets that are running on the computer.
The throttle limit applies only to the current cmdlet, not to the session or to the computer.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### Microsoft.Management.Infrastructure.CimInstance#MSFT_FSRMClassification

## NOTES

## RELATED LINKS

[Get-FsrmClassification](./Get-FsrmClassification.md)

[New-FsrmScheduledTask](./New-FsrmScheduledTask.md)

[Start-FsrmClassification](./Start-FsrmClassification.md)

[Stop-FsrmClassification](./Stop-FsrmClassification.md)

[Wait-FsrmClassification](./Wait-FsrmClassification.md)
