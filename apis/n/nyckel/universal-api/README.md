# <img src="https://images.mindcloud.co/apps/icons/nyckel_1775668650550.png" alt="Nyckel logo" width="28" height="28"> Nyckel: Universal API

Build, run, and improve custom ML functions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nyckel/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nyckel.com/
- **Vendor API docs:** https://www.nyckel.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Functions](actions/list-functions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/list-functions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a new field in Nyckel. |
| [Delete Field](actions/delete-field.md) | DELETE | Deletes an existing field from Nyckel. |
| [Get Field](actions/get-field.md) | GET | Retrieves a field from Nyckel. |
| [List Fields](actions/list-fields.md) | GET | Retrieves fields from Nyckel. |
| [Update Field](actions/update-field.md) | PUT | Updates an existing field in Nyckel. |

### Function

| Action | Method | Description |
| --- | --- | --- |
| [Create Function](actions/create-function.md) | POST | Creates a new function in Nyckel. |
| [Delete Function](actions/delete-function.md) | DELETE | Deletes an existing function from Nyckel. |
| [Get Function](actions/get-function.md) | GET | Retrieves a function from Nyckel. |
| [List Functions](actions/list-functions.md) | GET | Retrieves functions from Nyckel. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [Create Label](actions/create-label.md) | POST | Creates a new label in Nyckel. |
| [Delete Label](actions/delete-label.md) | DELETE | Deletes an existing label from Nyckel. |
| [Get Label](actions/get-label.md) | GET | Retrieves a label from Nyckel. |
| [List Labels](actions/list-labels.md) | GET | Retrieves labels from Nyckel. |
| [Update Label](actions/update-label.md) | PUT | Updates an existing label in Nyckel. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Function Summary](actions/get-function-summary.md) | GET | Retrieves a function summary from Nyckel. |

### Sample

| Action | Method | Description |
| --- | --- | --- |
| [Create Text Sample](actions/create-text-sample.md) | POST | Creates a text sample in Nyckel. |
| [Delete Sample](actions/delete-sample.md) | DELETE | Deletes an existing sample from Nyckel. |
| [Get Sample](actions/get-sample.md) | GET | Retrieves a sample from Nyckel. |
| [List Samples](actions/list-samples.md) | GET | Retrieves samples from Nyckel. |

### Sample Annotation

| Action | Method | Description |
| --- | --- | --- |
| [Delete Sample Annotation](actions/delete-sample-annotation.md) | DELETE | Deletes a sample annotation from Nyckel. |
| [Set Sample Annotation](actions/set-sample-annotation.md) | PUT | Updates a sample annotation in Nyckel. |

