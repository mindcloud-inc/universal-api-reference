# ACLU Universal API Examples

These examples use the MindCloud API key and ACLU connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Node By NID

Retrieves a Torture Database node by numeric ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aCLU/latest/actions/get-node-by-nid?connectionId=$CONNECTION_ID&nid=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nid": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aCLU/latest/actions/get-node-by-nid?${params}`, {
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
      "field_doc_date": [
        {}
      ],
      "field_doc_description": [
        {}
      ],
      "field_doc_draft": [
        {}
      ],
      "field_doc_foia": [
        {}
      ],
      "field_doc_handwritten_text": [
        {}
      ],
      "field_doc_id": [
        {}
      ],
      "field_doc_pdf": [
        {}
      ],
      "field_doc_release_date": [
        {}
      ],
      "field_doc_text": [
        {}
      ],
      "nid": 1,
      "path": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Node By NID action reference](actions/get-node-by-nid.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aCLU/latest/actions/get-node-by-nid).
