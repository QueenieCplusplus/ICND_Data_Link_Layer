# ICND Data Link Layer
資料鏈結層

在資料被送到線上傳輸之前，就必須註明它要送到何處並且促成什麼結果，這些功能便是在此層完成的。

* 橋接器

功能等同於第二層交換器，拜 ASIC 晶片控制速度（快過軟體），故能達到十億位元的傳輸速度。
不同於集線器，此類設備能分割不同的廣播/碰撞區（網段）。

當橋接器收到 frame，會以 LLC 和 MAC 的方式處理該訊息。此類網路設備可決定收到的訊息是否轉送到其它網段，每回收到經過此區段的訊息，並從其中學習到各發送端 nodes 所在的區段與位址。並將這些學習到的資料彙整成傳送位址表 forwarding table，因為傳送位址表中列出了所有端點的位址（取自封包來源位址），與它所在的網路區段，每當橋接器收到一 frame 時，橋接器便檢查了接收端的位址，並且與 forwarding table 紀錄比較 match ，藉此決定要過濾、傳送、擴散到另一區段。

* 下三層 （資料流）     


詳見 OSI 7 Layer

https://github.com/QueenieCplusplus/ICND_OSI_7Layer#osi-七-層

                               
                 packet          Network // IP, IPX                    IP header
                 
                 
                 
                 
                 
                                                                       LLC header (logical link control)
                               
                 frame           DataLink // 802.3
                 
                                                                       MAC header 
                                                                       
                                                                       
                                                                       
                                                                       
                             
                 bits            Physical /* move bits between devices */

本層的主要目的在提供工作站，位於線路上 bits 之上的第一邏輯層溝通，由於它在資料欄位中註明了端點 end point 的 MAC address 實體位置，網路上的各設備方才能決定是否要將收到的訊息往通訊協定堆疊之上一層傳送，且決定哪一項通訊協定，資料鏈結層支援各種連結導向 connection-oriented 或是 非連結導向的服務如 connectionless。

關於 IEEE 區分的兩個子層為：

* LLC 邏輯連結控制

此層能藉由代碼 type code 、 服務存取點 sap id，區分不同的通訊協定，並將資料封裝成相對應的格式。 至於到底使用何種資料框，則取決於更上層的通訊協定。

利用序號控制位元 sequence control bit ，在某些通訊協定中，取代了 Transport Layer 功能，能定義何種服務為可靠或是不可靠。

* MAC 網路（媒體）存取控制

此層定義了實體位置、frame 的傳送次序、錯誤通知、流量控制。


