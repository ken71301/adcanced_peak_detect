# adcanced_peak_detect

改良peak detect演算法(於資策會)


基於scipy的peak detect，增加移動閥值檢測與判斷靜止閥值，提高peak detect的可用性。

由於移動閥值檢測，可以將不同振福的波型同時考慮，scipy的pead detection只能針對單一高度做分辨。

靜止閥值為可選，由於感測器得知的波型或多或少有雜訊(如靜止時訊號)，而濾波器又無法精準將雜訊濾掉時，可用單純的靜止閥值取代濾波器的部分公用。


自行開發測試介面(於資策會)


基於上述修改之peak detect，使用PyQt開發簡易介面，方便不熟悉演算法之使用者能根據使用情境修改不同參數，同時以此介面連接API，令使用者能即時得知修改後結果，並能將結果存進MongoDB中。



如附圖所示：使用者於上方輸入參數後，將出現波型經過peak detect後之圖形，其中紅色線即為改良演算法得出之移動閥值結果，若因資料過於偏差導致有未判讀或誤判之位置，使用者也可以自行以此程式修改。

![image](https://github.com/ken71301/adcanced_peak_detect/blob/main/peakdetect1.jpg)

![image](https://github.com/ken71301/adcanced_peak_detect/blob/main/peakdetect2.jpg)
