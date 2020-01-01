# OSI 7層模型

## Layer 1: Physical Layer
```
[1]實體層是真正負責將binary資料(bit)傳送到網路
[2]涵蓋傳輸媒介，資料傳送技術，以及資料編碼技巧

傳輸媒介
雙絞線 (Twisted pair)
同軸電纜線 (Coaxial cable)
光纖 (Fiber-optic)

資料編碼 (Encoding) :
如何在傳輸線上表示所欲傳送的二進位資料
何種訊號代表 "1"，何種訊號又代表 "0"。
範例:在某些電報系統中，傳輸線上出現一個「脈衝」(Pulse) 代表一個位元的 "1"，沒有出現脈衝則代表一個 "0"

```
## Layer 2: Data Link Layer
```
[1]使用實體傳輸設備將資料傳送到網路上
並將結果毫無錯誤的上傳給網路層，
主要負責相鄰兩點間的可靠傳送

[2]功能:
切割框架(framing)
流量控制(flow control)
錯誤控制(error control)
定義完整服務給網路層連結(Connection)關係管理
媒體存取控制(MAC) Medium Access Control

IEEE 802.3(乙太網)
HDLC,FRAME Relay,PPP,FDDI,ATM,IEEE802.5/802.2
```
## Layer 3: Network Layer
```
[1]網路層提供遞送及其他相關功能，讓您能將多條網路連線結合為大型的互連網路

[2]四大功能:
決定路徑
定址(addressing):Classful vs CIDR
被遞送協定(routed protocol)與地送協定(routed protocol,路由協定)
異性質遞送(Heterogeneous Routing)

屬於網路層的協定有：
ARP (Address Resolution Protocol)--位址解析協定
RARP (Reverse Address Resolution Protocol)—反位址解析協定
IP (Internet Protocol)—網際網路協定
ICMP(Internet Control Message Protocol)—網際網路控制訊息協定
IGMP(Internet Group Message Protocol)—網際網路群組訊息協定

```
## Layer 4: Transport Layer
```
[1]負責進行流量控制(fiow control)與傳輸，會將Session層送來的資訊切割(Segment)及重組(reassemble)回原本的資料流(data stream)

[2]提供端點對端點的傳輸服務


[3]TCP 提供 保證(guaranteed)的資料傳送
   所以發生錯誤的資料要重傳
[4] UDP 提供  無保證(unguaranteed)的資料傳送

TCP ( Transport Control Protocol) 傳輸控制協定(可靠性)
UDP (User Datagram Protocol)使用者資料片協定(丟了不管)

```
## Layer 5: Session Layer
```
[1]會談層負責應用程式間會談的起始、控制、及結束。允許不同機器間建立session並維持session的進行

[2]所有的通訊會談都始於服務要求(request)，並由會談層協定進行控制，以完成目標網路裝置之應用的服務回應(server response)

[3]會談層也會控制兩個應用間的通訊。決定在特定時間，應該由哪個程序進行傳送或接收

```
## Layer 6: Presentation Layer
```
[1]表現層的目的是要保證從來源機器送出的資料，能夠被目標機器讀取。
因為存在許多不同的系統，且每個系統看資料的方式都不相同，因此需要該層以確保資料能轉換成可被讀取的形式

[2]功能:
資訊語法、語意
各種電腦內碼轉換與編碼
資料壓縮(Data Compression)
加解密。

JPEG,
ASCII,
EBCDIC,
TIFF,
GIF,
PICT,
cncryption,
MPEG,
MIDI
```
## Layer 7: Application Layer
```
[1]應用層負責提供使用者程序(user process)
與協定堆疊(protocol stack)溝通的方法。
提供使用者功能，以完成各項應用。

[2]功能:
提供WWW,
檔案移轉(FTP)
電子郵遞(Email)
遠端登入(telnet)

有許多協定======不同功能
Telnet
HTTP | HTTP2 | HTTPs
FTP |sFTP
NFS
SMTP|POP3
SNMP
LDAP

```
