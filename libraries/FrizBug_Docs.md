
# **FrizBug Docs**

## method: str(`input`)
```
method str(any input) => string
```  
Converts all types to respective `string` form    
**Parameters**   
- `input` - (any) required    
>  
**`Returns`**  
string of the input
***

## method: init(`console`)
```
method init(string console='table') => array<string>
```  
Initiation of console array  
**Parameters**  
- `console` - (string) indicating the type of console to output data to. Valid options are `'table'`, `'label'`, `'box'`, and `'tool'`. The default value is `'table'`.  
>  
**`Returns`**  
Console stirng[]
***

## method: update(`console1`, `console2`, `console3`)
```
update(array<string> console1=na,array<string> console2=na,array<string> console3=na 
|    color bg_color=#0000007d,color text_color=#00ff00,color border_color=#00ff00) => Void
```   
The update function updates the given consoles with the latest input in their respective buffers.  
It also checks for the type of console and updates the label, table, box, or tooltip accordingly.  
If a console is not provided or is empty, it is skipped.  
**Parameters**  
- `console1` - (string) An array of strings representing the console to be updated.  
- `console2` - (string) An array of strings representing the console to be updated.  
- `console3` - (string) An array of strings representing the console to be updated.  
- `bg_color` - (color) Color of the bg of the console  
- `text_color` - (color) Color of the text of the console 
- `border_color` - (color) Color of the border of the console 
> 
**`Returns`**  
(void)
***

## method: log(`console`, `inp`, `data_label`, `off`, `loop`, `tick`, `m_rows`, `a_index`, `m_rows`, `m_cols`)
```
method log(array<string> console,any inp,string data_label="",bool off=false,
|    int loop=na,bool tick=false) => inp param (unchanged)
```  
Log and keep records of log events  
**Parameters**  
- `console` - (array<string>) The console to output the message to.  
- `inp` - (all) The input value to be printed.  
- `data_label` - (string) An optional label to be printed before the input value.  
- `off` - (bool) An optional flag to turn off printing. Default is `false`.  
- `loop` - (int) for the index inside a loop will display the index on the console.  
- `tick` - (bool) An optional flag to turn off printing. Default is `false`.  
- `a_index` - (int) An optional parameter for printing an array with a specified number of indexs. 
- `m_rows` - (int) An optional parameter for printing a matrix with a specified number of rows.  
- `m_cols` - (int) An optional parameter for printing a matrix with a specified number of columns.  
> 
**`Returns`**  
the `inp` param of the function    
***

## method: print(`input`, `data_label`, `tick`, `pos`, `off`, `loop`, `a_index`, `m_rows`, `m_cols`, `size`, `text_size`, `bg_color`, `text_color`)
```
method print(any input, string data_label='',bool tick=false, string pos=na,  
|   bool off=false, int loop=na, int size=20, string text_size=size.small, 
|   color bg_color=#0000007d, color text_color=#00ff00) => input param (unchanged)
```   
Print single variable per bar data. To print more than 1 data the data must be called together.

There is no need to init and database or to update at the end of script.

the only drawback is that you can only view 1 variable at a time for each position unless an array or a matrix is used.

**Parameters**   
- `input` - (all) The input to be printed in the console    
- `data_label` - (string) A label to be printed before each input in the console. Default value is an empty string.  
- `tick` - (bool) A flag indicating whether to print the input immediately [`true`] or store it in a buffer to be printed. Default value is false.  
- `pos` - (string) The position of the console on the chart. Valid values are `"1"`, `"2"`, `"3"`, `"4"`, `"5"`, `"6"`, `"7"`, `"8"`, a corresponding to the positions in a 3x3 grid. If set to `na`, the console will be placed in the bottom. Default value is `na`.  
- `off` - (bool) A flag indicating whether to disable printing [`true`] or enable it [`false`]. Default value is `false`.  
- `a_index` - (int) An optional parameter for printing an array with a specified number of indices. 
- `m_rows` - (int) An optional parameter for printing a matrix with a specified number of rows.  
- `m_cols` - (int) An optional parameter for printing a matrix with a specified number of columns.  
- `size` - (int) The maximum number of lines that can be displayed in the console. Default value is `20`.  
- `loop` - (int) for the index inside a loop will display the index on the console.  
- `text_size` - (string) The size of the text in the console. Default value is `size.small`.  
- `bg_color` - (color) The background color of the console. Default value is `#0000007d`.  
- `text_color` - (color) The color of the text in the console. Default value is `#00ff00`.  
>  
**`Returns`**  
the `input` param of the function
***
## Credits:
@kaigouthro - for the font library  
@RicardoSantos - for the Debugging Concept that I used to make this
***
Everything should be pretty simple.  
Just use
```
bug.print([tick or console], val, (label if you want))
bug.console([tick or console], val, (label if you want))
```