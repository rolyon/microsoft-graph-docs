---
title: "plannerUser resource type"
description: "The **plannerUser** resource provides access to Planner resources for a user. "
localization_priority: Normal
author: "TarkanSevilmis"
ms.prod: "planner"
---

# plannerUser resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The **plannerUser** resource provides access to Planner resources for a [user](user.md). 


## Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[List tasks](../api/planneruser-list-tasks.md) |[plannerTask](plannertask.md) collection| Get the [plannerTasks](plannertask.md) assigned to the user.|
|[List favoritePlans](../api/planneruser-list-favoriteplans.md) |[plannerPlan](plannerplan.md) collection| Get the [plannerPlans](plannerplan.md) marked as favorite by the user.|
|[List recentPlans](../api/planneruser-list-recentplans.md) |[plannerPlan](plannerplan.md) collection| Get the [plannerPlans](plannerplan.md) recently viewed by the user.|
|[Update](../api/planneruser-update.md) | [plannerUser](planneruser.md)| Update a **plannerUser** object. |


## Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|id|String| Read-only. Identifier of the plannerUser|
|favoritePlanReferences|[plannerFavoritePlanReferenceCollection](plannerfavoriteplanreferencecollection.md)| A collection containing the references to the plans that the user has marked as favorites.|
|recentPlanReferences|[plannerRecentPlanReferenceCollection](plannerrecentplanreferencecollection.md)| A collection containing references to the plans that were viewed recently by the user in apps that support recent plans.|

## Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|tasks|[plannerTask](plannertask.md) collection| Read-only. Nullable. Returns the [plannerTasks](plannertask.md) assigned to the user.|
|favoritePlans|[plannerPlan](plannerplan.md) collection| Read-only. Nullable. Returns the [plannerPlans](plannerplan.md) that the user marked as favorites.|
|recentPlans|[plannerPlan](plannerplan.md) collection| Read-only. Nullable. Returns the [plannerPlans](plannerplan.md) that have been recently viewed by the user in apps that support recent plans. |

## JSON representation
The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerUser"
}-->

```json
{
  "favoritePlanReferences": {"@odata.type": "microsoft.graph.plannerFavoritePlanReferenceCollection"},
  "id": "String (identifier)",
  "recentPlanReferences": {"@odata.type": "microsoft.graph.plannerRecentPlanReferenceCollection"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "plannerUser resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/planneruser.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
