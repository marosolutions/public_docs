# JETSEND API
[API Docs](https://docs.jetsend.com/)

## Get List of Templates

### RequestURL:
```
GET https://app.jetsend.com/api/v1/email_templates
```

### Request Header:
```json
{"authorization":"Bearer mysupersecretapikey", "Content-Type":"application/json"}
```

### Request Payload:
```json
{}
```

### Response Payload:
```json
{
    "data": [
        {
            "id": "d8308111-3b8f-4c9b-9417-55b891333882",
            "account_id": "02f4a6f9-51aa-438d-8c9c-f5b61ced70e4",
            "name": "Test-template",
            "subject": "test-template",
            "from_email": "anant@example.com",
            "from_name": "anant",
            "reply_to": "",
            "status": "draft",
            "html": "<!DOCTYPE html>\n<html lang = \"en-US\">\n  <head>\n    <meta charset = \"utf-8\">\n    <title>My test page</title>\n    \n    <style>\n      form {\n        margin : 0 auto;\n        width: 400px;\n        padding : 1em;\n        border : 1px solid #CCC;\n        border-radius : 1em;\n      }\n      \n      ul {\n        list-style : none;\n        padding : 0;\n        margin : 0;\n      }\n      \n      form li + li {\n        margin-top : 1em;\n      }\n      \n      label {\n        display : inline-block;\n        width : 90px;\n        text-align : right;\n      }\n      \n      input, textarea {\n        font : 1em sans-serif;\n        width : 300px;\n        box-sizing : border-box;\n        border : 1px solid #999;\n      }\n      \n      input : focus, textarea : focus {\n        border-color : #000;\n      }\n      \n      textarea {\n        vertical-align : top;\n        height : 5em;\n      }\n      \n      .button {\n        padding-left : 90px;\n      }\n      \n      button {\n        margin-left : .5em;\n      }\n      \n    </style>\n  </head>\n  <body>\n    <p>This is my page</p>\n    <form action = \"/my-handling-form-page\" method = \"post\">\n      <ul>\n        <li>\n          <label for = \"name\">Name:</label>\n          <input type = \"text\" id = \"name\" name = \"user_name\">\n        </li>\n        \n        <li>\n          <label for = \"mail\">E-mail:</label>\n          <input type = \"email\" id = \"mail\" name = 'user_mail'>\n        </li>\n        \n        <li>\n          <label for = \"msg\">Message:</label>\n          <textarea id = \"msg\" name = \"user_message\"></textarea>\n        </li>\n        \n        <li class = \"button\">\n          <button type = \"submit\">Send your message</button>\n        </li>\n      </ul>\n    </form>\n  </body>\n</html>",
            "text": "",
            "headers": {},
            "created_at": "2024-01-16T10:36:10.698-05:00",
            "updated_at": "2024-01-16T10:36:10.698-05:00"
        },
        {
            "id": "7a17ec08-1a0b-4a8d-a59c-6c23d3776eaf",
            "account_id": "02f4a6f9-51aa-438d-8c9c-f5b61ced70e4",
            "name": "testtemplate",
            "subject": "test content",
            "from_email": "testqa@prodtest.com",
            "from_name": "test",
            "reply_to": "",
            "status": "draft",
            "html": "<h>hiiiiiiiii<h>",
            "text": "",
            "headers": {},
            "created_at": "2021-05-04T02:13:24.795-04:00",
            "updated_at": "2021-05-04T02:13:24.795-04:00"
        },
        {
            "id": "ff53f9a7-4e87-48ba-b389-2dd4ea4cfa4f",
            "account_id": "02f4a6f9-51aa-438d-8c9c-f5b61ced70e4",
            "name": "test",
            "subject": "Template test email",
            "from_email": "qa@prodtest.com",
            "from_name": "test qa",
            "reply_to": "",
            "status": "draft",
            "html": "<!DOCTYPE html PUBLIC \"-//W3C//DTD HTML 4.01//EN\">\n<html>\n<head>\n  <title>My first styled page</title>\n</head>\n\n<body>\n\n<!-- Site navigation menu -->\n<ul class=\"navbar\">\n  <li><a href=\"index.html\">Home page</a>\n  <li><a href=\"musings.html\">Musings</a>\n  <li><a href=\"town.html\">My town</a>\n  <li><a href=\"links.html\">Links</a>\n</ul>\n\n<!-- Main content -->\n<h1>My first styled page</h1>\n\n<p>Welcome to my styled page!\n\n<p>It lacks images, but at least it has style.\nAnd it has links, even if they don't go\nanywhere\u0026hellip;\n\n<p>There should be more here, but I don't know\nwhat yet.\n\n<!-- Sign and date the page, it's only polite! -->\n<address>Made 5 April 2004<br>\n  by myself.</address>\n\n</body>\n</html>\n",
            "text": "",
            "headers": {},
            "created_at": "2021-01-28T04:07:26.506-05:00",
            "updated_at": "2021-01-28T04:07:26.506-05:00"
        }
    ],
    "meta": {
        "page": 1,
        "per_page": 25,
        "total_pages": 1,
        "total_count": 3
    }
}
```

## Get a Template by Name

### RequestURL:
```
GET https://app.jetsend.com/api/v1/email_template
```

### Request Header:
```json
{"authorization":"Bearer mysupersecretapikey", "Content-Type":"application/json"}
```

### Request Payload:
```json
{
    "name": "mytemplate"
}
```

### Response Payload:
```json
{
  "id": "4c0e01c4-88c8-4142-ac6d-409e7560d533",
  "account_id": "31ff7331-7v7d-4750-a367-0ecdf215aff6",
  "name": "mytemplate",
  "subject": "Email Template",
  "from_email": "user@example.com",
  "from_name": "bob",
  "reply_to": "user1@example.com",
  "status": "draft",
  "html": "<p>Hi {{customer_type}} \nSave big this Christmas in your area {{place}}! \nClick http://www.mysite.com and get a {{discount}}% discount\n</p><p>Hurry, this offer is only to {{user_type}}\n</p>",
  "text": "Save big this Christmas in your area {{place}}!",
  "headers": {},
  "created_at": "2020-06-09T10:44:20.634-04:00",
  "updated_at": "2020-06-01T00:19:02.137-04:00"
}
```

## Send an Email

## Request URL:
```
POST https://app.jetsend.com/api/v1/transmission/email
```

## Request Header:
```json
{"Authorization":"Bearer mysupersecretapikey","Content-Type":"application/json"}
```

## Request Data:
```json
{
  "email": {
    "options": {
      "description": "Christmas Campaign Email",
      "campaign_id": "my_campaign",
      "open_tracking": true,
      "click_tracking": true,
      "tracking_domain": "jetsend.abc.com",
      "skip_suppression": false,
      "inline_css": false
    },
    "metadata": {
      "user_type": "students",
      "education_level": "college"
    },
    "substitution_data": {
      "discount": "25"
    },
    "tags": [
      "cat",
      "dog"
    ],
    "recipients": [
      {
        "address": {
          "email": "anant@example.com",
          "name": "Wilma Flintstone"
        },
        "tags": [
          "cat",
          "dog"
        ],
        "substitution_data": {
          "customer_type": "Platinum"
        },
        "metadata": {
          "age": "24",
          "place": "Bedrock"
        }
      }
    ],
    "content": {
      "template_id": "",
      "email_rfc822": "",
      "from": {
        "name": "Fred Flintstone",
        "email": "fred@example.com"
      },
      "subject": "Big Christmas savings!",
      "reply_to": "Jetsend Support <support@jetsend.com>",
      "headers": {
        "X-Customer-Campaign-ID": "christmas_campaign"
      },
      "text": "Save big this Christmas in your area {{place}}!",
      "html": "<a href='https://www.w3schools.com'>click me again</a>"
    }
  }
}
```

## Response:
```json
{
    "transmission_id": "ec2eac27-7093-4af3-afe4-37c6129723b2"
}
```
