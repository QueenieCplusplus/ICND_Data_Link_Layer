# ICND Data Link Layer
資料鏈結層

在資料被送到線上傳輸之前，就必須註明它要送到何處並且促成什麼結果，這些功能便是在此層完成的。

詳見 OSI 7 Layer

https://github.com/QueenieCplusplus/ICND_OSI_7Layer#osi-七-層

下三層 （資料流）                
                               
                 packet          Network // IP, IPX                    IP header
                 
                 
                                                                       LLC header (logical link control)
                               
                 frame           DataLink // 802.3
                 
                                                                       MAC header 
                             
                 bits            Physical /* move bits between devices */

本層的主要目的在提供工作站，位於線路上 bits 之上的第一邏輯層溝通，由於它在資料欄位中註明了端點 end point 的 MAC address 實體位置，網路上的各設備方才能決定是否要將收到的訊息往通訊協定堆疊之上一層傳送，且決定哪一項通訊協定，資料鏈結層支援各種連結導向 connection-oriented 或是 非連結導向的服務如 connectionless。

關於 IEEE 區分的兩個子層為：

* LLC 

* MAC
