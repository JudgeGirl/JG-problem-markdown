## 歡迎光臨, 計算機程式設計課之批改娘系統 ##


* CSIE 1210 雙班 加簽授權碼 於 2015/09/15 Tue. 起至 ** 資 332 實驗室 ** 找 TA 拿取 (限有在課堂上 ** 到場登記 ** 加簽的同學)。
* 請各位同學拿取到發送到信箱密碼後自行修改密碼
	* 登入 -> BXXXXXX (點選自己的帳號) -> EDIT PROFILE 完成修改。

##  聯絡資訊 ##

* [Facebook 林小明 TA 粉絲頁](https://www.facebook.com/ntucsiec2014xiaominglin)
* [課程網頁](https://sites.google.com/site/ntucsiec2015/)
* [dplabta@gmail.com](dplabta@gmail.com) 課程相關問題

## 工作站 ##

```
$ ssh b01902000@linux1.csie.ntu.edu.tw
```

```
$ vim first_problem.c
<< keyboard pressed 'i' into the insert mode
#include <stdio.h>
int main() {
	puts("hello, world");
	return 0;
}
```

```
$ gcc first_problem.c -o first.out
$ ./first.out
>> hello, world
```

## Fast Start - Macbook/Ubuntu ##

* 打開 Termainl (終端機)，下達 `pwd` 指令可以得到當前所在目錄位置
```
morris:~ morris$ pwd
>> /Users/morris
```

* 假設 `hello.c` 檔案放至桌面目錄下，執行 `cd ~/Desktop`，其中 `~` 表示從家目錄下。
```
morris:~ morris$ cd ~/Desktop
morris:Desktop morris$ 
```

* 可以利用 Editor 或者是 command line mode 下的 vim 編譯器創建文字欓。
```
morris:Desktop morris$ vim hello.c
```
進入 vim 不要慌，仔細看左下角的訊息，按下鍵盤上的 `i` 可以進入 `-- INSERT --` 模式，這時候可以打上你的程式碼，按下鍵盤上的 `ESC` 離開 INSERT MODE。最後按下 `:wq` (寫入並離開) 或者是 `:q` (離開) 又或者是 `:q!` (離開但不儲存) 才能關閉 vim 編譯器。

* 編譯 `hello.c` 檔案，預設會產出 `./a.out` 的執行檔。
```
morris:Desktop morris$ gcc hello.c -std=c99
```

* 測試運行
```
morris:Desktop morris$ ./a.out
```

## Fast Start - Common ##

* 進入無限迴圈，強制關閉運行
	* 若按下 `Ctrl + Z + ENTER` 相當於 stdin 串流的 EOF
	* 若按下 `Ctrl + C` 相當於中斷程式
	* 若按下 `Ctrl + D` 相當於前兩個合併一起處理
* 鍵入檔案名稱打入很慢，請善用利用 `Tab` 鍵提供自動補完
* 指令很長，要回到行首或行尾修改參數，請善用 `HOME` 和 `END` 鍵。Macbook 使用者若在 Terminal 請使用 `control + a` 和 `control + e`，若在 Editor 上則使用 `command + ←` 和 `command + →`

## Example Code ##

```
#include <stdio.h>

int main() {
	int a, b;
	while (scanf("%d %d", &a, &b) == 2)
		printf("%d\n%d\n", b, a);
	return 0;
}
```