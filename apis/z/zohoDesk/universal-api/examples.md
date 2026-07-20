# Zoho Desk Universal API Examples

These examples use the MindCloud API key and Zoho Desk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Profile

Retrieve the configuration details and permissions defined for the profile of the currently logged in user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/get-my-profile?${params}`, {
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
      "default": true,
      "description": "string",
      "id": 1,
      "isVisible": true,
      "name": "Ava Chen",
      "permissions": {
        "accounts": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "import": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "activities": {
          "deleteSharedCustomViews": true,
          "editSharedCustomViews": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true
        },
        "agents": {
          "create": true,
          "delete": true,
          "edit": true,
          "import": true,
          "overview": true,
          "viewAllFields": true
        },
        "calls": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "import": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "chat": {
          "view": true
        },
        "clientAction": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "clientActionConditions": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "clientActionLocationAssociation": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "clientActionModuleAssociation": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "clientEvents": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "comments": {
          "delete": true,
          "deleteOthers": true,
          "edit": true,
          "editOthers": true
        },
        "community": {
          "create": true,
          "delete": true,
          "edit": true,
          "moderate": true,
          "view": true
        },
        "communityComment": {
          "view": true
        },
        "communityTopic": {
          "view": true
        },
        "componentEventMappingAssociation": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "componentMapping": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "contacts": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "import": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "contracts": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "import": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "courses": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "crmInteg": {
          "crmAccountsActivityCalls": true,
          "crmAccountsActivityEvents": true,
          "crmAccountsActivityTasks": true,
          "crmAccountsInfo": true,
          "crmAccountsNotes": true,
          "crmAccountsPotentials": true,
          "crmContactsActivityCalls": true,
          "crmContactsActivityEvents": true,
          "crmContactsActivityTasks": true,
          "crmContactsInfo": true,
          "crmContactsNotes": true,
          "crmContactsPotentials": true
        },
        "eventMapping": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "events": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "import": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "financeInteg": {
          "createContact": true,
          "createEstimate": true,
          "createInvoice": true,
          "createSalesOrder": true,
          "sendEstimate": true,
          "sendInvoice": true,
          "sendSalesOrder": true,
          "viewEstimate": true,
          "viewInvoice": true,
          "viewSalesOrder": true,
          "viewSubscription": true
        },
        "gc": {
          "create": true,
          "delete": true,
          "edit": true,
          "view": true
        },
        "im": {
          "create": true,
          "delete": true,
          "edit": true,
          "view": true
        },
        "imConversations": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "imMessages": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "kbCategory": {
          "admin": true,
          "create": true,
          "delete": true,
          "edit": true,
          "editAllArticles": true,
          "export": true,
          "import": true,
          "manageKB": true,
          "view": true
        },
        "managerDashboard": {
          "allView": true,
          "customize": true,
          "myView": true
        },
        "mobileapp": {
          "customMobileApps": true,
          "deskapp": true,
          "radar": true
        },
        "modules": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "products": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "import": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "radar": {
          "activities": true,
          "agentStats": true,
          "apiUsageAlerts": true,
          "auditLog": true,
          "averageHandlingTime": true,
          "channelTraffic": true,
          "contacts": true,
          "currentStats": true,
          "customerHappiness": true,
          "dailyToast": true,
          "dailyTrend": true,
          "dashboards": true,
          "exceptionHandling": true,
          "fcr": true,
          "feeds": true,
          "im": true,
          "kb": true,
          "liveTraffic": true,
          "manageRadar": true,
          "mostThreadedTickets": true,
          "quickView": true,
          "textContentProtection": true,
          "visualContentProtection": true
        },
        "reports": {
          "create": true,
          "delete": true,
          "edit": true,
          "export": true,
          "view": true
        },
        "setup": {
          "automation": true,
          "buttons": true,
          "chat": true,
          "community": true,
          "customerHappiness": true,
          "department": true,
          "email": true,
          "exportPortalUsers": true,
          "exportUsers": true,
          "featureConfig": true,
          "fetchAcrossDepartment": true,
          "gamification": true,
          "globalReports": true,
          "googleAnalytics": true,
          "im": true,
          "importHistory": true,
          "layouts": true,
          "localization": true,
          "manageAgents": true,
          "manageMarketplace": true,
          "managerDashboard": true,
          "massComment": true,
          "massReply": true,
          "moveRecords": true,
          "permission": true,
          "pinnedConversations": true,
          "portal": true,
          "portalUsers": true,
          "privacySettings": true,
          "rebranding": true,
          "recycleBin": true,
          "sandbox": true,
          "securitySettings": true,
          "shareSnippet": true,
          "signUpApproval": true,
          "social": true,
          "tabsAndFields": true,
          "teams": true,
          "telephony": true,
          "templates": true,
          "timeTracking": true,
          "webForm": true,
          "webhooks": true
        },
        "social": {
          "twitterConversationReply": true,
          "twitterPostCreate": true,
          "twitterPostDelete": true,
          "view": true
        },
        "supportEmailAddress": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "tasks": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "import": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "ticketLifeCycleData": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "tickets": {
          "addFollowers": true,
          "changeOwner": true,
          "closeTicket": true,
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "deleteTags": true,
          "edit": true,
          "editSharedCustomViews": true,
          "editTags": true,
          "export": true,
          "handleUnassigned": true,
          "import": true,
          "mailReview": true,
          "mailSend": true,
          "manageOwnCustomViews": true,
          "mergeTickets": true,
          "reshareSharedCustomViews": true,
          "revokeBlueprint": true,
          "shareOwnCustomViews": true,
          "shareTickets": true,
          "unassignedChangeOwner": true,
          "view": true
        },
        "timeEntry": {
          "create": true,
          "delete": true,
          "edit": true,
          "view": true
        },
        "zia": {
          "create": true,
          "delete": true,
          "edit": true,
          "view": true
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get My Profile action reference](actions/get-my-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoDesk/latest/actions/get-my-profile).

## Create Account



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountName": "Ava Chen"
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
      "accountName": "Ava Chen",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "phone": "string",
      "website": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Account action reference](actions/create-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoDesk/latest/actions/create-account).
