# <img src="https://images.mindcloud.co/apps/icons/formtaxi_1774960872841.png" alt="Form.taxi logo" width="28" height="28"> Form.taxi: Universal API

Read form submissions with API-key auth and create new Form.taxi form endpoints without prior authentication.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/formtaxi/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://form.taxi
- **Vendor API docs:** https://docs.form.taxi/en/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Form Submissions](actions/list-form-submissions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formtaxi/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&formCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Endpoint](actions/create-endpoint.md) | POST | Creates a new endpoint in Form.taxi. |

### Form Submission

| Action | Method | Description |
| --- | --- | --- |
| [List Form Submissions](actions/list-form-submissions.md) | GET | Retrieves form submissions from Form.taxi. |

