# <img src="https://images.mindcloud.co/apps/icons/id-dju-u-u4-logos_1775148850846.png" alt="Cloutly logo" width="28" height="28"> Cloutly: Universal API

Drive, monitor, respond to, and showcase customer reviews

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloutly/latest
- **Category:** Marketing
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloutly.com
- **Vendor API docs:** https://docs.cloutly.com/reviews-sdk-for-marketplace-websites

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Businesses](actions/list-businesses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/list-businesses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Business

| Action | Method | Description |
| --- | --- | --- |
| [Create Business](actions/create-business.md) | POST | Creates a new business in Cloutly. |
| [Get Business](actions/get-business.md) | GET | Retrieves business details from the Cloutly marketplace. |
| [Get Business OAuth Link](actions/get-business-oauth-link.md) | GET | Retrieves a business source auth link from Cloutly. |
| [List Businesses](actions/list-businesses.md) | GET | Retrieves businesses connected to your Cloutly account. |

### Health Check

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Verifies Cloutly API key authentication setup. |

### Review

| Action | Method | Description |
| --- | --- | --- |
| [List Reviews](actions/list-reviews.md) | GET | Retrieves reviews for connected sources in Cloutly. |

### Review Invite

| Action | Method | Description |
| --- | --- | --- |
| [Send Review Invite](actions/send-review-invite.md) | POST | Creates a customer review invite in Cloutly. |

