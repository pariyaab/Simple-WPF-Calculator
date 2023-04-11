# Simple-WPF-Calculator

In this project, I change a developed simple WPF calculator from this github page (https://github.com/dariuszdbr/CalculatorWpfMVVM) and add a power opeator to it.
This project is working and handling mathmatics operator with `math.mxparser` library and parse each of expression and calculate them by defining a regular expression.
In `CalculatorModel.cs` there is function which is called `Insert` that is responsible for matching expressions with regular pattern expressions and the only thing that we should do for adding power operation instead of percent is that changing this 
regular expression in this way :
 Regex.IsMatch(element, @"[+\-*/%,]" -> Regex.IsMatch(element, @"[+\-*/,^]"
 then it can recognize power inputs and calculate them.
 the next step for this purposse is chaning its UI: for this we should change "ButtonPercent" to "ButtionPower" and remove its listener and change its content.

