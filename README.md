# 玩yolo~辨識我家的貓咪-阿勒
  
下載後，將Lei.data、Lei.names檔案，以及leitrain、leitest、trainLei.txt、testLei.txt資料夾丟入\darknet-master\build\darknet\x64\data
  
並將yolov3-tiny-Lei.cfg_train、yolov3-tiny-Lei.cfg_test兩個檔案丟入\darknet-master\build\darknet\x64\cfg

因為GPU沒很好...記憶體不夠大...先用yolo-tiny，不過結果效果還不錯，可以辨識的出模型未看過的圖片

在cfg檔中可以自己調整模型的參數，不過classes須設成欲辨識類別數，yolo前的filters須設成( 類別 + 5 ) * 3

( 類別 + 5 ) * 3 公式解釋：

    其中5為Boundary box中心的x、y座標、以及長、寬再加上1個confidence score(模型預測這個區域是阿勒的信心(ง๑ •̀_•́)ง)

    3為Boundary box的個數，表示圖片中的每一格可以預測三個Boundary box
  
雖然leitest、testLei.txt裡面沒啥東西，但是可以視情況自己丟點圖片去當驗證資料集

![image](https://github.com/julia8468bd/Identify_yolov3/blob/master/%E8%BE%A8%E8%AD%98%E6%88%91%E5%AE%B6%E8%B2%93%E9%98%BF%E5%8B%92.jpg)
