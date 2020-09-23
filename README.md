<div align="center">

## \!\!\!\!\*\*\*Cool Roll\*\*\*\!\!\!\!


</div>

### Description

This is a really cool effect that you can add to make it so that when you click a minimize button, the form slides off the screen and a little mini form appears in the bottom left hand corner. When you click this mini forms title bar, the form appears again. A Very cool effect that I just figured out. (o:
 
### More Info
 
Follow these instructions.

1) Start up a new project in your VB.

2) Add a new form. (Form2)

3) Add a timer to Form 1 and set it's interval to 1 by pressing F4 to access the properties.

4) Make Form 1's Border Style "0 - None" and make Form 2's Border Style  "3 - Fixed Dialog".

5) Add a Label to Form 1. (Label1) Make it's caption "_" (For Minimize)

6) Make Form2's Property "ControlBox = False".

7) Make Form2's Property "Movable = False".

8) And MOST IMPORTANTLY, make Form2's Property "WindowState = "Minimized"

9) That's all, but remember to MINIMIZE YOUR VB WHEN RUNNING THIS CODE. Thanks. (o:


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[SeeD](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/seed.md)
**Level**          |Unknown
**User Rating**    |3.0 (75 globes from 25 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__1-1.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/seed-cool-roll__1-2929/archive/master.zip)





### Source Code

```
'Put this in Form1's General Declarations.
Private Sub Label1_Click()
  Timer1.Enabled = True
  Form2.Visible = True
End Sub
Private Sub Form_Load()
  Timer1.Enabled = False
End Sub
Private Sub Timer1_Timer()
  Form1.Top = Form1.Top + 60 'You can adjust the 60 to whatever you prefer. Highering it will make the form drop faster. (o:
  Form2.Enabled = True
End Sub
'Put this in Form2's General Declarations. (o:
Private Sub Form_Activate()
  Form1.Show
  Form2.Hide
  Form1.Top = (Screen.Height - Height) / 2
  Form1.Left = (Screen.Width - Width) / 2
  Form1.Timer1.Enabled = False
End Sub
```

