# Resource Records

This repository is intended to store CSV batches for Resource Records on PhiZone. The following content is also available [here](https://www.phi.zone/legal/en/copyright-policy).

## Active Defense Against Copyright Infringements

PhiZone has a built-in system that actively reports potential copyright infringements on user submissions. We store [Resource Records](https://www.phi.zone/resource-records) in our database, which help the system identify user submissions that need restricting or rejecting. A Resource Record is comprised of the following fields:

1. title;
2. type (i.e. `0` for "Music" and `1` for "Illustration");
3. edition type (i.e. `0` for "Original Ver.", `1` for "Author's Edit", and `2` for "Second-Party Edit");
4. name/origin of edition (e.g. "Arcaea Edit"; leaving blank is suggested when the edition type is `0`);
5. strategy (i.e. `0` for "Accept", `1` for "Make hidden", `2` for "Make locked", `3` for "Make hidden and locked", and `4` for "Reject");
6. author's name;
7. copyright owner's name;
8. source URL;
9. description (optional).

The system searches for Resource Records that match the title,  the edition (both the edition type and the name/origin of edition), and the author's name of a user submission, and that has a strategy other than "Accept". If any Resource Records satisfy these conditions, they will be displayed on the submission page and, if the user insists, on the info page of the submission. Moderators are responsible for implementing the strategy specified by the corresponding Resource Records. In cases where multiple Resource Records with different strategies match, moderators act upon the strictest one.

If you, as a copyright owner, want your content included in this system, please create a pull request at our repository [phizone-resource-records](https://github.com/PhiZone/phizone-resource-records) with a CSV file that contains information aforementioned. The file should be created within a directory titled as the (concise) name of the copyright owner, following a naming convention in the form of `<game/work>-<update/operation>.csv` (e.g. `lowiro/arcaea-imagining-after.csv`, `rayark/cytusii-5.0-update.csv`). An example for this CSV file is as follows:

```
Title,Type,Edition Type,Edition,Strategy,Author,Copyright Owner,Source,Description
Used to be,0,0,,4,KIVΛ,Rayark Inc.,https://www.youtube.com/watch?v=hGaJNvkRfo0,
Abstruse Dilemma,0,1,"""D"" side long ver.",4,Ashrount vs. 打打だいず,lowiro Ltd.,https://www.youtube.com/watch?v=7VOuvpq20NQ,
Sheriruth (Laur Remix),0,0,,4,Laur,"lowiro Ltd., Marvelous Inc. & HARDCORE TANO*C",https://www.youtube.com/watch?v=e09aoYJcNSU,
Einherjar Joker,0,1,Requiem EXTENDED MIX,4,DJ Genki vs Gram,lowiro Ltd. & HARDCORE TANO*C,https://www.youtube.com/watch?v=pdmtqN68vOg,
Wish Upon a Snow,0,0,,4,打打だいず,lowiro Ltd.,https://www.youtube.com/watch?v=0L0J8PhHy0E,"Winning entry in Arcaea Song Contest - 3rd Movement ""Imagining After""".
今年も「雪降り、メリクリ」目指して頑張ります！！,0,0,,4,AiSS vs. 华牧狸 w/ 夜輪 ft. 結月ゆかり,"Xiamen Pigeon Games Network Co., Ltd.",https://www.bilibili.com/video/BV1ic41157r1/,
```

Please adhere to the specified order of the fields as illustrated in the example and ensure that they are separated by commas without any spaces before or after them. To include commas in your data, enclose the field in quotation marks. To preserve in-data quotation marks, double them in a quoted field. Upon receiving the pull request, we will take action within 7 business days.

Alternatively, you may join our group chat on QQ ([714344319](https://h5.qun.qq.com/h5/qun-share-page/?_wv=1027&k=O2GbdboCc4etoeMMkJk8dCFVO6BueaKY&authKey=%2FZ810eNpglqIj6Ft7AJtVKHrZTP1VFmWVYQlvhhjur9s1IReWUXz38IqWDPwNRwF&market_channel_source=714344319_1&noverify=0&group_code=714344319)) to discuss related issues.
