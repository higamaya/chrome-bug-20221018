# chrome-bug-20221018

## Issue

Chrome crashes when calling setRangeText just before setSelectionRange on an input field element that has received focus.

## Steps that cause problems

1. Clone this repo.

2. Open [index.html](./index.html) in Chrome.

3. Click `Increase text` button several times.

4. When character counter exceeds 402, Chrome will crash.

## Environment

### OS

* Microsoft Windows 10 Pro 10.0.19044

### Browser

* Google Chrome 106.0.5249.119 (Official Build) (64-bit)
* Microsoft Edge 106.0.1370.47 (Official build) (64-bit)

## More practical case

I discovered this problem when I was implementing a feature where selecting text in an input field and entering double quotation marks would enclose the selected text in quotation marks.<br>
[putQuotesArroundSelectedTest.html](putQuotesArroundSelectedTest.html) is closer to that implementation (with a lot of simplifications though).<br>
[index.html](./index.html) has been created to further simplify and minimize code to reproduce the problem.

