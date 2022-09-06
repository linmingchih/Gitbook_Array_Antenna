---
description: >-
  SBR+為Shooting Bouncing
  Ray增強版，引擎計算將射線計算及場計算分開。射線計算可快速模擬出光的行進方向，但是無法模擬出強度分布。場計算則可以模擬並顯示空間當中場的變化狀況。極化在計算之內。
---

# HFSS SBR+

### SBR+的應用場景

主要用在大空間場域的電磁波分布模擬，像是ADAS，5G基地台與終端的電磁波連結狀況。

### SBR+的激發源

SBR+的激發源主要為天線的輻射場，可以是由其他HFSS天線設計所生成的輻射場，或是理論天B線的輻射場。激發源可為Tx或Rx，一張設計當中可以允許多個Tx, Rx。

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### SBR+物件網格

下圖是PEC物件的網格，可以看出SBR+只需表面網格即可計算射線的行進方向。射線無法進入金屬物件內部，因此金屬內部並不需要網格。介電物質內部為均勻之材料，也不需要網格。

由於SBR+是模擬射線在空氣中傳播，因此只有物件表面要網格，空氣不需要網格，因此也不需要定義Aiir Box。

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

### 收斂條件

SBR+模擬的網格是固定的，由模擬頻率及結構曲率決定。因此沒有收斂條件計算
