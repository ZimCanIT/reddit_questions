### Question 

* Does anyone have an idea asto how I can go about converting a.bak file into a .html file in python?
* [Source](https://www.reddit.com/r/learnpython/comments/vnk5v0/converting_file_types/?utm_source=share&utm_medium=web2x&context=3)

### Reason for asking

* When a profile is reset at my workplace, it often loses it's bookmarks. These are saved within an old profile folder called: "bookmarks.bak"
* I'd like to create a pythonic method of converting the .bak file into a `.html` file that can then be imported as a bookmark in chrome

### Content displayed in notepad when a .bak file is opened

```
{
   "checksum": "521379267296fdbe9691bf1798e7c90e",
   "roots": {
      "bookmark_bar": {
         "children": [ {
            "date_added": "13270643918398977",
            "guid": "4bfc1c49-0246-46a7-948d-a452ecd465a9",
            "id": "5",
            "name": "Cascade",
            "type": "url",
            "url": "https://rmguk.cascadecloud.co.uk/"
         }, {
            "date_added": "13271156402858774",
            "guid": "5ba86aea-71f7-4306-aa19-d7366281a231",
            "id": "7",
            "name": "Natterbox Wallboards",
            "type": "url",
            "url": "https://wbapp.natterbox.com/#/dashboard-admin/?id=6225-204906-d-1594542455519"
         }, {
            "date_added": "13271432592145397",
            "guid": "49d8f562-ade1-45ed-a2ec-ecf5f894b932",
            "id": "9",
            "name": "Teams",
            "type": "url",
            "url": "https://teams.microsoft.com/_?culture=en-us&country=WW&lm=deeplink&lmsrc=homePageWeb&cmpid=WebSignIn#/conversations/19:22c8c814-338d-44da-9f54-64bbb3d04354_3f32826e-1b0d-415a-96da-8e2422d0342f@unq.gbl.spaces?ctx=chat"
         }, {
            "date_added": "13272109684351058",
            "guid": "7dfbe687-cdff-4e71-b933-57bbeadb6436",
            "id": "11",
            "name": "SAP Concur Home",
            "type": "url",
            "url": "https://www.concursolutions.com/home.asp"
         }, {
            "date_added": "13272627545219688",
            "guid": "3269beb0-b433-424a-8e06-4b79b4f9a17c",
            "id": "13",
            "name": "Quote of the Day - BrainyQuote",
            "type": "url",
            "url": "https://www.brainyquote.com/quote_of_the_day"
         }, {
            "date_added": "13281528776908482",
            "guid": "625f3809-2b2b-400a-8452-a39a4a2e24cb",
            "id": "18",
            "name": "Wisdom Quotes",
            "type": "url",
            "url": "https://wisdomquotes.com/quote-of-the-day/"
         }, {
            "date_added": "13273323362382973",
            "guid": "ee7bf3eb-1b9e-4180-ab36-998e20366d9c",
            "id": "15",
            "name": "Meeting Room Booking",
            "type": "url",
            "url": "https://frameworkswestminster.skedda.com/booking"
         }, {
            "date_added": "13273323614797603",
            "guid": "ad4d4a09-89db-4fde-852e-d0f6da70b568",
            "id": "16",
            "name": "Frameworks",
            "type": "url",
            "url": "https://www.notion.so/Working-at-Frameworks-Westminster-21a5b38cbc9542848d604c8e22c46115"
         } ],
         "date_added": "13269442416778104",
         "date_modified": "13281528789092913",
         "guid": "0bc5d13f-2cba-5d74-951f-3f233fe6c908",
         "id": "1",
         "name": "Bookmarks bar",
         "type": "folder"
      },
      "other": {
         "children": [  ],
         "date_added": "13269442416778121",
         "date_modified": "0",
         "guid": "82b081ec-3dd3-529c-8475-ab6c344590dd",
         "id": "2",
         "name": "Other bookmarks",
         "type": "folder"
      },
      "synced": {
         "children": [  ],
         "date_added": "13269442416778124",
         "date_modified": "0",
         "guid": "4cf2e351-0e85-532b-bb37-df045d8f8d0f",
         "id": "3",
         "name": "Mobile bookmarks",
         "type": "folder"
      }
   },
   "sync_metadata": "CisKCwiIgQISBTQyNDA2EgAgASoYY0lLaXU5Yy9qUkk0c2hoS0duR0p0QT09EqsBCA0SpgEKHDhHdFZTVnpTY0JBdk5BNnV5dW9rNkxTbjNDND0SKjMyOTA0XzMyNjliZWIwLWI0MzMtNDI0YS04ZTA2LTRiNzliNGY5YTE3YxgAIAkoCTDYwwE4hLmmrLEvQMjE/ZrRL0oceHVmYnM3dHB5b2xxSnM2UHMyNUk5Yk1jQVBrPVofIh3qUHhSUlBXVS9zVXNCaGdxS1o4Zy9CaTJCTldFPWUbFWdHEqsBCAsSpgEKHEJ3YStTT2QveXMyclJyVjZYRG42aStkZHJxMD0SKjMyOTA0XzdkZmJlNjg3LWNkZmYtNGU3MS1iOTMzLTU3YmJlYWRiNjQzNhgAIAkoCTDVwwE4/9yuta8vQMbE/ZrRL0ocYldnNVY0WDVOSWZCYUFMbENjYklXR212QzNFPVofIh3UcUNIT29neituOEIyR1FZRmRGaVJ4elVJejUwPWW5CQWhEqoBCAUSpQEKHFE4ajZ2amM0Mms5c0VKNDgxb2JSQmE1cXJDQT0SKjMyOTA0XzRiZmMxYzQ5LTAyNDYtNDZhNy05NDhkLWE0NTJlY2Q0NjVhORgAIAooCjDUwwE4wLy3+qkvQMXE/ZrRL0ocUS9VazU1T2xNWW5vZXR4emRVMUdPQ0twaHpNPVoeIhw3U0Qwb3V3NVRDaUFQWkVtN1Q2NEZQZ05uQUE9ZfD/yFMSaggCEmYKHFljU1RvbnZFU1B3cUNzNEwyY3JWaHY2OEw5OD0SFTMyOTA0X290aGVyX2Jvb2ttYXJrcxgAIAAoADAEOABAAEocNXVzeS9jcGZwaTFFdG9CSERnWElzMHFiNHJBPVoAZQAAAAASqwEIEBKmAQoceVpYcHdDY0hCTWtWR1ZDeGxrWGE0ajVUTVVFPRIqMzI5MDRfYWQ0ZDRhMDktODlkYi00ZmRlLTg1MmUtZDBmNmRhNzBiNTY4GAAgECgQMKbLAjjPlJv4sy9Aw8u9soQwShxVN0NQQlBHZVZFMVhrNFVUOGowNVlKVVhLUjA9Wh8iHfpRVWZnN09SYXJKcnVzWXhRcEVDK05SeTVJazA9Zap4IAISqwEIEhKmAQocY1dGUEJMWis1Wm1nS1pvRnJRK3c3Ums0RVRRPRIqMzI5MDRfNjI1ZjM4MDktMmIyYi00MDBhLTg0NTItYTM5YTRhMmUyNGNiGAAgBSgFMNLDATjNwd7A0i9AioffwNIvShx1SHA3UEx6VHlaeWpiWXZxNFVqTHJvdENoTHc9Wh8iHfdvSUVQQkVET0RzRStHTlIxdXd3eFBnbitPNms9ZUYldq0SqwEIDxKmAQocM3FXTTJlRkNJbWdvRVl6MWE0UnFPUS9kcXBFPRIqMzI5MDRfZWU3YmYzZWItMWI5ZS00MTgwLWFiMzYtOTk4ZTIwMzY2ZDljGAAgDSgNMMPGATjQ4Iv4sy9A67SIwNMvShxFd0l2c3pQenUzYTVaQmJncTB1THNCS2MzQ2s9Wh8iHfhBcVY5UVpKa3ordnkzdmVsVHd6bk9mL1R1QlU9Za/SpnASqgEIBxKlAQocWlk5dmNOdjlEajdzTzNFZ1dRQ1FTZ1VWSEE0PRIqMzI5MDRfNWJhODZhZWEtNzFmNy00MzA2LWFhMTktZDczNjYyODFhMjMxGAAgCSgJMNfDATirhefuqy9AxcT9mtEvShxNNDZlY3NucFlCZ3p5N2d6RjdZdXlSdEV6TXc9Wh4iHFFwVVNvOExrV1Fxd3ZuYXZXeVNlVTVaa2JWZz1lorxxhxJnCAESYwoceXhKLzZmdmtlY3I3a3A1RVF6QjR0V0xwZGJFPRISMzI5MDRfYm9va21hcmtfYmFyGAAgACgAMAM4AEAAShxVK0dHSXRaRURwWnNJU2xPVWFJVHVJTGRNbkk9WgBlAAAAABKrAQgJEqYBChxTbHdjcjVnVUk4TXFWVFZtZFFHUlo1U3ZiOWs9EiozMjkwNF80OWQ4ZjU2Mi1hZGUxLTQ1ZWQtYTJlYy1lY2Y1Zjg5NGI5MzIYACAOKA4w1sMBOJKmwPKsL0DGxP2a0S9KHEJIN3FTVklXbTFEVXdDNWF3M0w5MXNpRXBXUT1aHyIdqC9Ta3ZrWHZYMTg2RDRFczZBdHZWWmx0TEZNcz1lk6qH2RJrCAMSZwocbmpnRHU4OGVDcnZYcDg2cEQ3ZkhHY3FGcDg4PRIWMzI5MDRfc3luY2VkX2Jvb2ttYXJrcxgAIAAoADAFOABAAEocNzlsK0xSRVVwaWFFdkREK0c0M2NwWFN0d0JjPVoAZQAAAAAwAQ==",
   "version": 1
}
```
