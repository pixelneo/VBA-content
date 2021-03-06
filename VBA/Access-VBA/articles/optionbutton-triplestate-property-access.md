---
title: OptionButton.TripleState Property (Access)
keywords: vbaac10.chm10578
f1_keywords:
- vbaac10.chm10578
ms.prod: access
api_name:
- Access.OptionButton.TripleState
ms.assetid: f2764290-00be-38f7-f078-fc0059340455
ms.date: 06/08/2017
---


# OptionButton.TripleState Property (Access)

You can use the  **TripleState** property to specify how the specified control will display Null values. Read/write **Boolean**.


## Syntax

 _expression_. **TripleState**

 _expression_ A variable that represents an **OptionButton** object.


## Remarks

The  **Null** property uses the following settings.



|**Setting**|**Description**|
|:-----|:-----|
|**True**|The control will cycle through states for Yes, No, and  **Null** values. The control appears dimmed (grayed) when its **Value** property is set to **Null**.|
|**False**|(Default) The control will cycle through states for Yes and No values.  **Null** values display as if they were No values.|
This property can be set in any view.


## Example

The following example displays a message describing in detail the state of a check box named "Check1" on the form "frmOperations". 


```vb
Dim strTripleState As String 
 
strTripleState = Forms.Item("frmOperations").Controls.Item("Check1").TripleState 
 
Select Case strTripleState 
 Case True 
 MsgBox "For Check1, TripleState = " &; strTripleState &; _ 
 ". The control will cycle through states for Yes, No, " &; _ 
 "and Null values. The control appears dimmed (grayed) " &; _ 
 "when its Value property is set to Null." 
 Case False 
 MsgBox "For Check1, TripleState = " &; strTripleState &; _ 
 ". The control will cycle through states for Yes and No " &; _ 
 "values. Null values display as if they were No values." 
 Case Else 
 MsgBox "Can't determine the TripleState property for Check1." 
End Select 

```


## See also


#### Concepts


[OptionButton Object](optionbutton-object-access.md)

