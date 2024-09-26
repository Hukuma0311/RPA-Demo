<!-- 底下標籤來源參考寫法可至：https://github.com/Envoy-VC/awesome-badges#github-stats -->

<!--[](https://img.shields.io/github/stars/hsiangfeng/README-Example-Template.svg)｜![](https://img.shields.io/github/forks/hsiangfeng/README-Example-Template.svg)｜![](https://img.shields.io/github/issues-pr/hsiangfeng/README-Example-Template.svg)｜![](https://img.shields.io/github/issues/hsiangfeng/README-Example-Template.svg)-->

**Read this in Traditional Chinese:[中文](README-ZH.md)**

# Using UiPath Studio to capture condensed financial statement from TWSE MOPS

*Warning: This is just a Demo Project of UiPath Studio. It may be discontinued at any moment.*

![專案封面圖](https://raw.githubusercontent.com/Hukuma0311/RPA-Demo/refs/heads/main/pic/logo.jpg)

## Description

This process will access to https://mops.twse.com.tw/mops/web/index and search for specific companies.  
It will capture the condense financial report and paste to a xlsx file and delete all columns except EPS and Book Value per Share.   

After capturing all stocks, the process will generate the line chart about EPS and Book Value per Share of the company, saving the file named of the capture date.  

In theory, You can capture companies as many as possible. I choose 3 companies for demo purpose.

> <!--此專案是一份 README 的撰寫範本，主要是方便所有人可以快速撰寫 README，讓大家可以更有方向的去寫出 README。--!>

- [Demo Video](https://www.youtube.com/watch?v=sqFJjTY6k6Y)

## Screenshots


*Capture Data*
![Capture Data](https://github.com/Hukuma0311/RPA-Demo/blob/main/pic/Sequence.jpg?raw=true)

*Data Process*
![Data Process](https://github.com/Hukuma0311/RPA-Demo/blob/main/pic/Excel%20Process%20Scope.jpg?raw=true)
*Final Result*
![Final Result](https://github.com/Hukuma0311/RPA-Demo/blob/main/pic/Final%20Result.png?raw=true)

## Installation

1. Download this repo and unzip it. 

2. Open the *Main.xaml* file and open the "Sequence"

3. Click "Variables" and edit company name you want in "stock". 

4. Back to Flowchart and open "Excel Process Scope". Edit the "To" path to the location you want to save the file.

5. Pulish this process to your local folder (I recommend publish to the same folder with other files.) You will see a file name which is ended with ".nupkg"

6. Run "RUN" on Windows by pressing "Win+R" and search "AppData". Find the    "UiRobot.exe" It should in the "C:\Users\[Your User]\AppData\Local\Programs\UiPath\Studio" Copy the Path.

 7. Edit the "Main.bat" in folder with Notepad. Edit the [ ] part like below.

```bash
"C:\Users\[Your User]\AppData\Local\Programs\UiPath\Studio\UiRobot.exe" execute --file "[location You Save this Porject]\[Name of the process you just publish].nupkg"
pause
```

8. Save it and Well done it might work like a charm!







