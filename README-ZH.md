<!-- 底下標籤來源參考寫法可至：https://github.com/Envoy-VC/awesome-badges#github-stats -->

<!--[](https://img.shields.io/github/stars/hsiangfeng/README-Example-Template.svg)｜![](https://img.shields.io/github/forks/hsiangfeng/README-Example-Template.svg)｜![](https://img.shields.io/github/issues-pr/hsiangfeng/README-Example-Template.svg)｜![](https://img.shields.io/github/issues/hsiangfeng/README-Example-Template.svg)-->

**以英文閱讀此說明:[English](README.md)**

# 利用UiPath Studio 擷取公開資訊觀測站之簡明財報資料

*注意: 此為UiPath Studio之示範專案，隨時可能停止更新*

![專案封面圖](https://raw.githubusercontent.com/Hukuma0311/RPA-Demo/refs/heads/main/pic/logo.jpg)

## 說明

此自動化流程會訪問[公開資訊觀測站](https://mops.twse.com.tw/mops/web/index)並搜尋指定之公開發行公司，擷取其近期之簡明財務資料，貼上至xlsx檔案中，並只留下EPS與每股淨值欄位

在擷取完所有公司後，會自動生成個股EPS與每股淨值折線圖，並以擷取日作為檔名存檔

理論上您可以擷取數間公司資料，我選了三間公司作為示範目的

> <!--此專案是一份 README 的撰寫範本，主要是方便所有人可以快速撰寫 README，讓大家可以更有方向的去寫出 README。--!>

- [示範影片](https://www.youtube.com/watch?v=sqFJjTY6k6Y)

## 截圖


*擷取資料*
![Capture Data](https://github.com/Hukuma0311/RPA-Demo/blob/main/pic/Sequence.jpg?raw=true)

*資料整理*
![Data Process](https://github.com/Hukuma0311/RPA-Demo/blob/main/pic/Excel%20Process%20Scope.jpg?raw=true)
*成果*
![Final Result](https://github.com/Hukuma0311/RPA-Demo/blob/main/pic/Final%20Result.png?raw=true)

## 安裝

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