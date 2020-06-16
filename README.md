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
