# _FileWriteFromArray
 EndIf    Next    For $I = $ISC_Index + 1 To $aFileRead[0]     $aHolder[$I] = $aFileRead[$I]    Next    For $I = $aFileRead[0] To $tmpIndex Step -1     If $aHolder[$I] = "" Then      _ArrayDelete($aHolder, $I)     EndIf    Next   EndIf   _ArrayDelete($aHolder, 0)   _FileWriteFromArray($ISC_FileName, $aHolder)  Else   Return SetError(1, 0, 0)  EndIf  Return SetError(0, 0, 1)
