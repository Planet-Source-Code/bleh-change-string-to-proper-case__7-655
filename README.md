<div align="center">

## Change String To Proper Case


</div>

### Description

I may be reinventing the wheel here, but so far I have yet to find a built in Delphi function that will convert a string to proper case. I found this code somewhere on the web a while back, lost it, and managed to recreate it last night.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[bleh](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/bleh.md)
**Level**          |Beginner
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |Delphi 5
**Category**       |[String Manipulation](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/string-manipulation__7-5.md)
**World**          |[Delphi](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/delphi.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/bleh-change-string-to-proper-case__7-655/archive/master.zip)





### Source Code

<p>
<font face="Verdana" size="2">
<b>NOTE:</b>Make sure to add "StrUtils" to your Uses section</p>
<p>
<font color="#008000">
function properCase(sBuffer: string):string; <br>
var<br>
&nbsp;&nbsp;&nbsp;&nbsp;iLen, iIndex: integer;<br>
begin<br>
&nbsp;&nbsp;&nbsp;&nbsp;iLen := Length(sBuffer);<br>
&nbsp;&nbsp;&nbsp;&nbsp;sBuffer:= Uppercase(MidStr(sBuffer, 1, 1)) + Lowercase(MidStr(sBuffer,2, iLen));<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;for iIndex := 0 to iLen do<br>
&nbsp;&nbsp;&nbsp;&nbsp;begin<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;if MidStr(sBuffer, iIndex, 1) = ' ' then<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;sBuffer := MidStr(sBuffer, 0, iIndex) + Uppercase(MidStr(sBuffer, iIndex + 1, 1)) + Lowercase(MidStr(sBuffer, iIndex + 2, iLen));<br>
&nbsp;&nbsp;&nbsp;&nbsp;end;<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;Result := sBuffer;<br><br>
end;<br>
</font></font></p>

