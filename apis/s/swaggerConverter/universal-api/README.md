# <img src="https://images.mindcloud.co/apps/icons/swagger-converter_1777645241694.png" alt="Swagger Converter logo" width="28" height="28"> Swagger Converter: Universal API

Convert Swagger definitions to OpenAPI 3.0

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/swaggerConverter/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://converter.swagger.io/
- **Vendor API docs:** https://converter.swagger.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Convert Definition by URL](actions/convert-definition-by-url.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swaggerConverter/latest/actions/convert-definition-by-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fpetstore.swagger.io%2Fv2%2Fswagger.json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Openapi Document

| Action | Method | Description |
| --- | --- | --- |
| [Convert Definition by Content](actions/convert-definition-by-content.md) | POST | Creates a converted OpenAPI document in Swagger Converter from input content. |
| [Convert Definition by URL](actions/convert-definition-by-url.md) | GET | Retrieves a converted OpenAPI document from Swagger Converter by source URL. |

