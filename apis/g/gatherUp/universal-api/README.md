# <img src="https://images.mindcloud.co/apps/icons/h-jki0gzu-400x400_1773870405060.jpeg" alt="GatherUp logo" width="28" height="28"> GatherUp: Universal API

Request, monitor, and reply to customer reviews and feedback

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gatherUp/latest
- **Category:** Marketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gatherup.com
- **Vendor API docs:** https://app.gatherup.com/api/doc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Businesses](actions/list-businesses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-businesses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Auto Feedback Request

| Action | Method | Description |
| --- | --- | --- |
| [Auto Feedback Requests](actions/auto-feedback-requests.md) | PUT | Updates auto feedback request settings in GatherUp. |

### Business

| Action | Method | Description |
| --- | --- | --- |
| [Create Business](actions/create-business.md) | POST | Creates a new business in GatherUp. |
| [Deactivate Business](actions/deactivate-business.md) | PUT | Deactivates an existing business in GatherUp. |
| [Delete Business](actions/delete-business.md) | DELETE | Deletes an existing business from GatherUp. |
| [Get Business](actions/get-business.md) | GET | Retrieves detailed business information from GatherUp. |
| [List Businesses](actions/list-businesses.md) | GET | Retrieves a list of businesses from GatherUp. |
| [Reactivate Business](actions/reactivate-business.md) | PUT | Reactivates an existing business in GatherUp. |
| [Search for Business ID](actions/search-for-business-id.md) | GET | Finds a business ID in GatherUp. |
| [Update Business](actions/update-business.md) | PUT | Updates an existing business in GatherUp. |

### Business Type

| Action | Method | Description |
| --- | --- | --- |
| [List Business Types](actions/list-business-types.md) | GET | Retrieves a list of business types from GatherUp. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in GatherUp. |
| [Create Multiple Customers](actions/create-multiple-customers.md) | POST | Creates multiple new customers in GatherUp. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from GatherUp. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves detailed customer information from GatherUp. |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from GatherUp. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in GatherUp. |

### Customer Reply

| Action | Method | Description |
| --- | --- | --- |
| [Reply to Customer](actions/reply-to-customer.md) | POST | Creates a reply to a customer in GatherUp. |

### Facebook Recommendation

| Action | Method | Description |
| --- | --- | --- |
| [List Facebook Recommendations](actions/list-facebook-recommendations.md) | GET | Retrieves Facebook recommendations received in GatherUp. |

### Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Get Feedbacks Received](actions/get-feedbacks-received.md) | GET | Retrieves received customer feedback from GatherUp. |
| [Update Customer Feedback](actions/update-customer-feedback.md) | PUT | Updates existing customer feedback in GatherUp. |

### Feedback History

| Action | Method | Description |
| --- | --- | --- |
| [List Show-Hide History](actions/list-show-hide-history.md) | GET | Retrieves show-hide history records from GatherUp. |

### Feedback Request

| Action | Method | Description |
| --- | --- | --- |
| [Send Customer Feedback Request](actions/send-customer-feedback-request.md) | POST | Creates a customer feedback request in GatherUp. |

### Feedback Response

| Action | Method | Description |
| --- | --- | --- |
| [List Feedback Responses](actions/list-feedback-responses.md) | GET | Retrieves a list of feedback responses from GatherUp. |

### Google Q&a

| Action | Method | Description |
| --- | --- | --- |
| [List Google Q&A](actions/list-google-qa.md) | GET | Retrieves Google Q&A entries from GatherUp. |

### Notification Email

| Action | Method | Description |
| --- | --- | --- |
| [Add Email to Receive Notifications](actions/add-email-to-receive-notifications.md) | POST | Adds a notification email address in GatherUp. |
| [Remove Email from Notifications](actions/remove-email-from-notifications.md) | DELETE | Deletes a notification email from GatherUp. |

### Online Review

| Action | Method | Description |
| --- | --- | --- |
| [List Online Reviews Received](actions/list-online-reviews-received.md) | GET | Retrieves a list of online reviews from GatherUp. |

### Online Review Link

| Action | Method | Description |
| --- | --- | --- |
| [Add Online Review Link](actions/add-online-review-link.md) | POST | Adds an online review link in GatherUp. |
| [List Online Review Links](actions/list-online-review-links.md) | GET | Retrieves online review links from GatherUp. |
| [Update Online Review Link URL](actions/update-online-review-link-url.md) | PUT | Updates an online review link URL in GatherUp. |

### Online Review Reply

| Action | Method | Description |
| --- | --- | --- |
| [Reply to Online Review](actions/reply-to-online-review.md) | POST | Creates a reply to an online review in GatherUp. |

### Survey Answer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Survey Answers](actions/get-customer-survey-answers.md) | GET | Retrieves customer survey answers from GatherUp. |

### Survey Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Business Survey Results](actions/get-business-survey-results.md) | GET | Retrieves business survey results from GatherUp. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in GatherUp. |
| [Deactivate User](actions/deactivate-user.md) | PUT | Deactivates an existing user in GatherUp. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from GatherUp. |
| [Reactivate User](actions/reactivate-user.md) | PUT | Reactivates an existing user in GatherUp. |
| [Set User Password](actions/set-user-password.md) | PUT | Updates a user password in GatherUp. |
| [Update User Information](actions/update-user-information.md) | PUT | Updates an existing user in GatherUp. |
| [Update User Managed Businesses](actions/update-user-managed-businesses.md) | PUT | Updates a user's managed businesses in GatherUp. |

