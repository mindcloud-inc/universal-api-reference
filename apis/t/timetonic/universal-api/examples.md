# Timetonic Universal API Examples

These examples use the MindCloud API key and Timetonic connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Info

Retrieves the current user information from Timetonic.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-user-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "createdVNB": "string",
      "req": "string",
      "sstamp": 1,
      "status": "string",
      "transactionId": "string",
      "userInfo": {
        "colors": {
          "bleuNuit": "string",
          "bleuTurquoise": "string",
          "bleuViolet": "string",
          "defaut": "string",
          "gray": "string",
          "green": "string",
          "jauneIndien": "string",
          "lilas": "string",
          "noir": "string",
          "orange": "string",
          "orangePastel": "string",
          "pink": "string",
          "red": "string",
          "roseBois": "string",
          "vertPastel": "string"
        },
        "companyAccountPlan": "string",
        "firstTime": true,
        "licence": "string",
        "nbBooks": 1,
        "projectID": 1,
        "rights": {
          "canCreateWorkspace": true
        },
        "sstamp": 1,
        "uC": "string",
        "uimgStamp": 1,
        "userPrefs": {
          "account": "string",
          "address": "string",
          "birthd": "string",
          "cie": "string",
          "city": "string",
          "companySize": "string",
          "country": "string",
          "fname": "Ava Chen",
          "globalAdd": true,
          "globalCalendar": true,
          "globalSearch": true,
          "ip": "string",
          "lang": "string",
          "lastConnection": "string",
          "licenceId": 1,
          "lname": "Ava Chen",
          "mail1": "string",
          "mail1ToConfirm": "string",
          "mail2": "string",
          "mail2ToConfirm": "string",
          "method": "string",
          "mob1": "string",
          "mob2": "string",
          "nbCol": 1,
          "newsletter": true,
          "notifMobile": "string",
          "openGrand": true,
          "origin": "string",
          "region": "string",
          "regiondf": "string",
          "replace": true,
          "sdate": "string",
          "secondsSincePreviousConnection": "string",
          "sector": {},
          "sex": "string",
          "slashd": true,
          "soundNotifications": true,
          "syncWithHubic": true,
          "timezone": "string",
          "twoFactor": true,
          "twoFactorSecret": "string",
          "tz": "string",
          "ucreatedon": "string",
          "ukey": "string",
          "until": "string",
          "vatn": "string",
          "zip": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Get User Info action reference](actions/get-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timetonic/latest/actions/get-user-info).

## Create Or Update Multiple Table Rows

Creates or updates multiple table rows in Timetonic.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/create-or-update-multiple-table-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookOwner": "string",
  "rows": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/create-or-update-multiple-table-rows', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookOwner": "string",
    "rows": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "createdVNB": "string",
      "formLastModified": 1,
      "newRows": [
        {}
      ],
      "readOnlyRowsStatus": [
        {}
      ],
      "req": "string",
      "rows": [
        {}
      ],
      "status": "string",
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Or Update Multiple Table Rows action reference](actions/create-or-update-multiple-table-rows.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timetonic/latest/actions/create-or-update-multiple-table-rows).
