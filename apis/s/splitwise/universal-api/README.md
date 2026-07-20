# <img src="https://images.mindcloud.co/apps/icons/splitwise_1773939422841.png" alt="Splitwise logo" width="28" height="28"> Splitwise: Universal API

Track shared expenses, balances, groups, and friends.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/splitwise/latest
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.splitwise.com/
- **Vendor API docs:** https://dev.splitwise.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new expense comment in Splitwise. |
| [Create Expense](actions/create-expense.md) | POST | Creates a new expense in Splitwise. |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes an expense comment from Splitwise. |
| [Delete Expense](actions/delete-expense.md) | DELETE | Deletes an existing expense from Splitwise. |
| [Get Expense](actions/get-expense.md) | GET | Retrieves expense details from Splitwise. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group's details from Splitwise. |
| [Get User](actions/get-user.md) | GET | Retrieves another user's details from Splitwise. |
| [List Expense Comments](actions/list-expense-comments.md) | GET | Retrieves comments for an expense in Splitwise. |
| [List Expenses](actions/list-expenses.md) | GET | Retrieves the current user's expenses from Splitwise. |
| [List Friends](actions/list-friends.md) | GET | Retrieves the current user's friends from Splitwise. |
| [List Groups](actions/list-groups.md) | GET | Retrieves the current user's groups from Splitwise. |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications from Splitwise. |
| [List Supported Categories](actions/list-supported-categories.md) | GET | Retrieves supported categories from Splitwise. |
| [List Supported Currencies](actions/list-supported-currencies.md) | GET | Retrieves supported currencies from Splitwise. |
| [Restore Expense](actions/restore-expense.md) | PUT | Restores a deleted expense in Splitwise. |
| [Update Expense](actions/update-expense.md) | PUT | Updates an existing expense in Splitwise. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user's details from Splitwise. |

