## Linkedin-Job-Profile-Scraper
A python library that uses browser automation to login & scrape job details from linkedin
It uses [datakund](https://pypi.org/project/datakund) internally

Complete Documentation available [here](https://linkedin-api.datakund.com/en/latest/)


### Support
For any help / feedback you can message us here
* datakund@gmail.com
* https://t.me/datakund

### Installation

```sh
pip install linkedin-job-profile-scraper
```

### Import

```javascript
from linkedin-job-profile-scraper import *
```

### Login

To scrape job details from linkedin first we will login to linkedin. There are two ways of login:-
* Credentials
* Cookies

#### Credentials

```javascript
linkedin.login(email="",password="")
```

#### Cookies

```javascript
linkedin.login_cookie(cookies="list_of_cookies")
```

##### Example Cookies

To login with cookies [Edit this Cookie Extension](https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg?hl=en) can be added to browser and login to linkedin.com , then export cookies and paste in above function of ``login_cookie``. Below is the example of cookies.

```[
{
    "domain": "linkedin.com",
    "expirationDate": 1671116358.392265,
    "hostOnly": false,
    "httpOnly": false,
    "name": "__Secure-3PAPISID",
    "path": "/",
    "sameSite": "no_restriction",
    "secure": true,
    "session": false,
    "storeId": "0",
    "value": "Y1zkx3HJhktM4Y__/A-aOUDHse1TaSaKpQ",
    "id": 1
},
{
    "domain": "linkedin.com",
    "expirationDate": 1672322803.302724,
    "hostOnly": false,
    "httpOnly": true,
    "name": "__Secure-3PSID",
    "path": "/",
    "sameSite": "no_restriction",
    "secure": true,
    "session": false,
    "storeId": "0",
    "value": "5AcqKCt5MuBkjOpLW7PdfNs83knLqt-qVZJzCriY_4_cftxmyExDbYRS65ezLjpKa_Xc7Q.",
    "id": 2
},
...
...

]
```

### Scrape Job details

To scrape job details from linkedin we use ``get_job_profile`` function.
It requires **job_link** as input parameter

```javascript
response=linkedin.get_job_profile(job_link="job_link_here")
job_details=response['body']
```

### Example Response

```sh
{

}
```

### DataKund
It uses [datakund](https://pypi.org/project/datakund/) internally to do browser automation
DataKund is an automation library that uses selenium & supports automation of many sites including [Youtube](https://youtube-api.datakund.com/en/latest/), [Amazon](https://amazon-api.datakund.com/en/latest/), [Twitter](https://twitter-api.datakund.com/en/latest/), [LinkedIn](https://linkedin-api.datakund.com/en/latest/) , [Google](https://google-api.datakund.com/en/latest/) etc.
