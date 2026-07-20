# SMS Connexion Universal API Examples

These examples use the MindCloud API key and SMS Connexion connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Balance

Retrieves the current account balance from SMS Connexion.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-account-balance?${params}`, {
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
      "balance": 1,
      "billing": "string",
      "currency": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Balance action reference](actions/get-account-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMSConnexion/latest/actions/get-account-balance).

## Add Contact To Optouts

Adds contacts to the optout list in SMS Connexion.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/add-contact-to-optouts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneNumbers": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/add-contact-to-optouts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneNumbers": {}
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
      "info": {},
      "invalid": [
        "string"
      ],
      "phoneNumbersByCountry": {},
      "totalDuplicates": 1,
      "totalInvalid": 1,
      "totalPhoneNumbers": 1,
      "totalValid": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Contact To Optouts action reference](actions/add-contact-to-optouts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMSConnexion/latest/actions/add-contact-to-optouts).
