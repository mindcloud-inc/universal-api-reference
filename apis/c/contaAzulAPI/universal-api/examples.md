# Conta Azul Universal API Examples

These examples use the MindCloud API key and Conta Azul connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Connected Company



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-connected-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-connected-company?${params}`, {
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
      "dataFundacao": "2026-05-07T12:00:00.000Z",
      "documento": "string",
      "email": "ava@example.com",
      "nomeFantasia": "string",
      "razaoSocial": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Connected Company action reference](actions/get-connected-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/contaAzulAPI/latest/actions/get-connected-company).
