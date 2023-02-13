<h1>Write-Up PTITCTF 2023</h1>
# Level 1 pwn

- Đầu tiên chúng ta quăng file vào Ghidra để coi mã giả.

<br>
<img src="./pseudo-code.png" alt="pseudo-code"/>
<br>

- Đọc code từ dưới lên thì ta thấy rằng để có được flag thì biến `xor` = `IamHaCer!!`
- Kéo tiếp lên trên thì ta thấy rằng biến `xor` chính là kết quả của phép xor giữa `something` (input thứ 2) và `source` (Data của chương trình)
- Ấn vào `source` để coi thử nó là gì ...

<img src="./source.png" alt="source"/>
<br>

- Dịch hết mã đó qua ASCII thì chúng ta được đoạn text như sau `>R!+Q.VEHr`
- Như vậy chúng ta đã tìm được `source`. Bây giờ để tìm biến `something` thì chúng ta xor biến `source` với biến `xor`
<br>

