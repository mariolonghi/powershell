---
applicable: SharePoint Online
external help file: PnP.PowerShell.dll-Help.xml
Module Name: PnP.PowerShell
online version: https://docs.microsoft.com/powershell/module/sharepoint-pnp/get-pnpcustomaction
schema: 2.0.0
title: Get-PnPCustomAction
---

# Get-PnPCustomAction

## SYNOPSIS
Return user custom actions

## SYNTAX

```
Get-PnPCustomAction [-Identity <GuidPipeBind>] [-Scope <CustomActionScope>]
 [-ThrowExceptionIfCustomActionNotFound] [-Web <WebPipeBind>] [-Connection <PnPConnection>]
 [-Includes <String[]>] [<CommonParameters>]
```

## DESCRIPTION
Returns all or a specific user custom action

## EXAMPLES

### EXAMPLE 1
```powershell
Get-PnPCustomAction
```

Returns all custom actions of the current site.

### EXAMPLE 2
```powershell
Get-PnPCustomAction -Identity aa66f67e-46c0-4474-8a82-42bf467d07f2
```

Returns the custom action with the id 'aa66f67e-46c0-4474-8a82-42bf467d07f2'.

### EXAMPLE 3
```powershell
Get-PnPCustomAction -Scope web
```

Returns all custom actions for the current web object.

## PARAMETERS

### -Connection
Optional connection to be used by the cmdlet. Retrieve the value for this parameter by either specifying -ReturnConnection on Connect-PnPOnline or by executing Get-PnPConnection.

```yaml
Type: PnPConnection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
Identity of the CustomAction to return. Omit to return all CustomActions.

```yaml
Type: GuidPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
Scope of the CustomAction, either Web, Site or All to return both

```yaml
Type: CustomActionScope
Parameter Sets: (All)
Aliases:
Accepted values: Web, Site, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrowExceptionIfCustomActionNotFound
Switch parameter if an exception should be thrown if the requested CustomAction does not exist (true) or if omitted, nothing will be returned in case the CustomAction does not exist

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

### -Web
The web to apply the command to. Omit this parameter to use the current web.

```yaml
Type: WebPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### List<Microsoft.SharePoint.Client.UserCustomAction>

## NOTES

## RELATED LINKS

[SharePoint Developer Patterns and Practices](https://aka.ms/sppnp)