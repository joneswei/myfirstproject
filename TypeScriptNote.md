TypeScript 學習筆記
==

摘錄自 [TypeScript 中文教學手冊](https://github.com/kkbruce/TypeScript/blob/master/doc/zh-tw/Handbook.md#1.4)


選擇性屬性的好處之一是可以對可能存在的屬性進行預定義，好處之二是可以捕獲使用了不存在的屬性時的錯誤。 比如，我們故意將拼寫錯誤的屬性名傳入createSquare，就會得到一個錯誤提示。

        interface SquareConfig {
          color?: string;
          width?: number;
        }   
        function createSquare(config: SquareConfig): {color: string; area: number} {
        var newSquare = {color: "white", area: 100};
        if (config.color) {
            newSquare.color = config.collor;  // 型別檢查器會查出這個拼寫錯誤
        }
        if (config.width) {
            newSquare.area = config.width * config.width;
        }
        return newSquare;
        }
        var mySquare = createSquare({color: "black"});



函數型別

介面能夠描述JavaScript中物件擁有的各種各樣的形體。 除了描述帶有屬性的普通物件外，介面也可以描述函數型別。

為了使用介面表示函數型別，我們需要給介面定義一個呼叫簽章。它就像是一個只有參數列表和回傳型別的函式定義。

