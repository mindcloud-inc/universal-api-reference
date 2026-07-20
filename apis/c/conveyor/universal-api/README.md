# <img src="https://images.mindcloud.co/apps/icons/images_1776178222020.png" alt="Conveyor logo" width="28" height="28"> Conveyor: Universal API

Manage trust centers, questionnaires, documents, and authorization workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/conveyor/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.conveyor.com
- **Vendor API docs:** https://docs.conveyor.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Connections](actions/list-connections.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-connections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Access Reviews

| Action | Method | Description |
| --- | --- | --- |
| [Create Authorization](actions/create-authorization.md) | POST | Creates an authorization in Conveyor from email or request. |
| [Create Review](actions/create-review.md) | POST |  |
| [Get Authorization Request](actions/get-authorization-request.md) | GET | Retrieves an authorization request from Conveyor. |
| [Ignore Authorization Request](actions/ignore-authorization-request.md) | PUT | Marks an authorization request as ignored in Conveyor. |
| [List Authorization Requests](actions/list-authorization-requests.md) | GET | Retrieves authorization requests from Conveyor with optional filters. |
| [List Authorizations](actions/list-authorizations.md) | GET | Retrieves authorizations from Conveyor with optional filters. |
| [List Open Authorization Requests](actions/list-open-authorization-requests.md) | GET | Retrieves open authorization requests from Conveyor. |
| [Update Authorization](actions/update-authorization.md) | PUT | Updates or revokes an authorization in Conveyor. |

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [List Interactions](actions/list-interactions.md) | GET | Retrieves interactions for a program from Conveyor. |
| [List Interactions By Connection](actions/list-interactions-by-connection.md) | GET | Retrieves interactions for a connection from Conveyor. |
| [List Interactions By Document](actions/list-interactions-by-document.md) | GET | Retrieves interactions for a document from Conveyor. |
| [List Interactions By Question](actions/list-interactions-by-question.md) | GET | Retrieves interactions for a knowledge base question from Conveyor. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [List Connections](actions/list-connections.md) | GET | Retrieves connections from Conveyor with optional filters. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a document in the Conveyor exchange. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from the Conveyor exchange. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from the Conveyor exchange. |
| [Update Document](actions/update-document.md) | PUT | Updates a document in the Conveyor exchange. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a folder in the Conveyor exchange. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes a folder from the Conveyor exchange. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from the Conveyor exchange. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Questionnaire](actions/create-questionnaire.md) | POST | Creates a questionnaire record in Conveyor. |
| [Create Questionnaire Request](actions/create-questionnaire-request.md) | POST | Creates a questionnaire request in Conveyor. |
| [List Questionnaires](actions/list-questionnaires.md) | GET | Retrieves questionnaires from Conveyor with optional filters. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Access Groups](actions/list-access-groups.md) | GET | Retrieves access groups for a program from Conveyor. |

### Knowledge Articles

| Action | Method | Description |
| --- | --- | --- |
| [List Knowledge Base Questions](actions/list-knowledge-base-questions.md) | GET | Retrieves knowledge base questions from Conveyor. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Product Lines](actions/list-product-lines.md) | GET | Retrieves product lines for a program from Conveyor. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Answer Single Question](actions/answer-single-question.md) | POST | Answers a one-off question in Conveyor. |

