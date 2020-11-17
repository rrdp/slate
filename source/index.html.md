---
title: MeetWell API
language_tabs:
  - json: JSON
  - shell: cURL
---


# Action Items

Action or Parking Lot Items

## Create action item


### Request

#### Endpoint

```plaintext
POST /api/v1/meetings/7747/action_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2YzNjNDAzNS1lOGY3LTRhZTYtYmQ5OC04ZWFlNGRlNWY3MGIiLCJzdWIiOiIxNjU0OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOSwiZXhwIjoxNjA3NjQ1NzI5fQ.kPECNznrDCE0VOetTMSk4ImUqSt7isoXlCdvXUUxuIM
```

`POST /api/v1/meetings/:meeting_id/action_items`

#### Parameters


```json
{"data":{"type":"action_item","attributes":{"description":"Discuss reticulating the splines.","owner_id":16548,"creator_id":16548,"category":"action_item","position":3,"due_by":"2020-11-17T00:15:29.390Z"}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| creator_id  | User id of person who created or suggested item |
| due_by  | Due date for addressing item |
| category  | Options: parking_lot or action_item (default) |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "291",
    "type": "action_items",
    "attributes": {
      "id": 291,
      "category": "action_item",
      "owner_name": "Doctor Jack of Hearts XI Agent Omega Red Girl",
      "owner_id": 16548,
      "description": "Discuss reticulating the splines.",
      "creator_id": 16548,
      "due_by": "2020-11-17T00:15:29.390Z",
      "position": 3,
      "creator_name": "Doctor Jack of Hearts XI Agent Omega Red Girl"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/7747/action_items" -d '{"data":{"type":"action_item","attributes":{"description":"Discuss reticulating the splines.","owner_id":16548,"creator_id":16548,"category":"action_item","position":3,"due_by":"2020-11-17T00:15:29.390Z"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2YzNjNDAzNS1lOGY3LTRhZTYtYmQ5OC04ZWFlNGRlNWY3MGIiLCJzdWIiOiIxNjU0OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOSwiZXhwIjoxNjA3NjQ1NzI5fQ.kPECNznrDCE0VOetTMSk4ImUqSt7isoXlCdvXUUxuIM"
```
## Delete action item


### Request

#### Endpoint

```plaintext
DELETE /api/v1/meetings/7746/action_items/290
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxYjQ0YzRhZC1hZGUyLTRkNTMtOWNjMi01ZTEwYTc4YTQ4OTkiLCJzdWIiOiIxNjU0NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOSwiZXhwIjoxNjA3NjQ1NzI5fQ.4DXgO-IwTw8NjCefvmQJCP4yI98jvZV5WG0cRHc51jk
```

`DELETE /api/v1/meetings/:meeting_id/action_items/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| creator_id  | User id of person who created or suggested item |
| due_by  | Due date for addressing item |
| category  | Options: parking_lot or action_item (default) |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/meetings/7746/action_items/290" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxYjQ0YzRhZC1hZGUyLTRkNTMtOWNjMi01ZTEwYTc4YTQ4OTkiLCJzdWIiOiIxNjU0NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOSwiZXhwIjoxNjA3NjQ1NzI5fQ.4DXgO-IwTw8NjCefvmQJCP4yI98jvZV5WG0cRHc51jk"
```
## List action items


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7744/action_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NGUxM2U4MS1jZGY4LTQyZWUtYmQwZC04NzI0YTNkNjNlMmIiLCJzdWIiOiIxNjUzOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOCwiZXhwIjoxNjA3NjQ1NzI4fQ.LOK3D0hC904GF1TGTRJhR8VHpM2CIH5vgbbgHyPXKAs
```

`GET /api/v1/meetings/:meeting_id/action_items`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| creator_id  | User id of person who created or suggested item |
| due_by  | Due date for addressing item |
| category  | Options: parking_lot or action_item (default) |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "288",
      "type": "action_items",
      "attributes": {
        "id": 288,
        "category": "action_item",
        "owner_name": "The Silverclaw Mr Exodus",
        "owner_id": 16540,
        "description": "Chicharrones waistcoat heirloom post-ironic listicle wolf muggle magic godard.",
        "creator_id": 16541,
        "due_by": "2020-11-18T00:15:28.493Z",
        "position": null,
        "creator_name": "Chuck Norris Space Ghost"
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7744/action_items" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NGUxM2U4MS1jZGY4LTQyZWUtYmQwZC04NzI0YTNkNjNlMmIiLCJzdWIiOiIxNjUzOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOCwiZXhwIjoxNjA3NjQ1NzI4fQ.LOK3D0hC904GF1TGTRJhR8VHpM2CIH5vgbbgHyPXKAs"
```
## Show action item


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7748/action_items/292
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3M2YwNDhhZS1kNjFhLTRiYzktYTUyOS1mY2QzYzhjOTk4NDAiLCJzdWIiOiIxNjU0OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOSwiZXhwIjoxNjA3NjQ1NzI5fQ.xH-G2eKhiLJnuCG_j6ld2YUlOTKm-SLndLrTGHqSFq0
```

`GET /api/v1/meetings/:meeting_id/action_items/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| creator_id  | User id of person who created or suggested item |
| due_by  | Due date for addressing item |
| category  | Options: parking_lot or action_item (default) |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "292",
    "type": "action_items",
    "attributes": {
      "id": 292,
      "category": "action_item",
      "owner_name": "Toad She-Hulk Man",
      "owner_id": 16550,
      "description": "Banh mi loko roof squid cornhole freegan plaid brooklyn.",
      "creator_id": 16551,
      "due_by": "2020-11-18T00:15:29.814Z",
      "position": null,
      "creator_name": "Bloodhawk Brain Cypher Woman"
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7748/action_items/292" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3M2YwNDhhZS1kNjFhLTRiYzktYTUyOS1mY2QzYzhjOTk4NDAiLCJzdWIiOiIxNjU0OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOSwiZXhwIjoxNjA3NjQ1NzI5fQ.xH-G2eKhiLJnuCG_j6ld2YUlOTKm-SLndLrTGHqSFq0"
```
## Update action item


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/7745/action_items/289
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmZWFkZjg2Yi0yZTY1LTRiMWUtYWUwZi05YmUxZTk3YzEyNjciLCJzdWIiOiIxNjU0MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOCwiZXhwIjoxNjA3NjQ1NzI4fQ.bo5vgOhSPbG-STLVsH2rjmgdcvfutRZ4wZnJjzAixzw
```

`PUT /api/v1/meetings/:meeting_id/action_items/:id`

#### Parameters


```json
{"data":{"type":"action_item","attributes":{"description":"Talk.","owner_id":16542,"creator_id":16542,"category":"action_item","position":2,"due_by":"2020-11-17T00:15:28.649Z"}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| creator_id  | User id of person who created or suggested item |
| due_by  | Due date for addressing item |
| category  | Options: parking_lot or action_item (default) |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "289",
    "type": "action_items",
    "attributes": {
      "id": 289,
      "category": "action_item",
      "owner_name": "The Match IX Gog of Hearts",
      "owner_id": 16542,
      "description": "Talk.",
      "creator_id": 16542,
      "due_by": "2020-11-17T00:15:28.649Z",
      "position": 2,
      "creator_name": "The Match IX Gog of Hearts"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/7745/action_items/289" -d '{"data":{"type":"action_item","attributes":{"description":"Talk.","owner_id":16542,"creator_id":16542,"category":"action_item","position":2,"due_by":"2020-11-17T00:15:28.649Z"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmZWFkZjg2Yi0yZTY1LTRiMWUtYWUwZi05YmUxZTk3YzEyNjciLCJzdWIiOiIxNjU0MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOCwiZXhwIjoxNjA3NjQ1NzI4fQ.bo5vgOhSPbG-STLVsH2rjmgdcvfutRZ4wZnJjzAixzw"
```
# Actions



## List future actions


### Request

#### Endpoint

```plaintext
GET /api/v1/future_actions?by_period[starts_at]=2020-11-06+00%3A15%3A23+UTC&amp;by_period[ends_at]=2020-12-06+00%3A15%3A23+UTC&amp;starts_at=2020-11-06+00%3A15%3A23+UTC&amp;ends_at=2020-12-06+00%3A15%3A23+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3Y2Y4NjQxYy0xYzBiLTQ0ZWYtYjkyYy0wYTUyN2Q0NWM1NWYiLCJzdWIiOiIxNjUwOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMywiZXhwIjoxNjA3NjQ1NzIzfQ.7IMMHXJp9KbiNqZraJM9aa5-MVwmyWJTCQz8CVtbhTg
```

`GET /api/v1/future_actions`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-11-06 00:15:23 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-12-06 00:15:23 UTC&quot;}
starts_at: 2020-11-06 00:15:23 UTC
ends_at: 2020-12-06 00:15:23 UTC
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "3238",
      "type": "future_actions",
      "attributes": {
        "meeting_id": 7738,
        "compliance_deadline": "2020-11-17T18:15:23.466Z",
        "details_negative": {
          "required_agenda": "This meeting needs an agenda",
          "required_objectives": "An objective is missing. What is the aim of the meeting? Understanding the goal for the meeting helps attendees engage.",
          "required_intention": "Missing a intention"
        },
        "organizer_email": "mauricio.barrows@armstrong.biz",
        "organizer_notes": null,
        "user_declined": false,
        "user_declined_at": null,
        "action_organizer_warned": false,
        "action_organizer_warned_at": null,
        "action": "remind",
        "meeting_summary": "Shabby chic kogi helvetica actually celiac.",
        "meeting_starts_at": "2020-11-18T00:15:23.466Z"
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/future_actions?by_period[starts_at]=2020-11-06+00%3A15%3A23+UTC&by_period[ends_at]=2020-12-06+00%3A15%3A23+UTC&starts_at=2020-11-06+00%3A15%3A23+UTC&ends_at=2020-12-06+00%3A15%3A23+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3Y2Y4NjQxYy0xYzBiLTQ0ZWYtYjkyYy0wYTUyN2Q0NWM1NWYiLCJzdWIiOiIxNjUwOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMywiZXhwIjoxNjA3NjQ1NzIzfQ.7IMMHXJp9KbiNqZraJM9aa5-MVwmyWJTCQz8CVtbhTg"
```
## List past actions


### Request

#### Endpoint

```plaintext
GET /api/v1/past_actions?by_period[starts_at]=2020-11-06+00%3A15%3A33+UTC&amp;by_period[ends_at]=2020-12-06+00%3A15%3A33+UTC&amp;starts_at=2020-11-06+00%3A15%3A33+UTC&amp;ends_at=2020-12-06+00%3A15%3A33+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5NDliYzBhMS01NWYxLTQ1NWYtOTVmMS0zNzU1MDQ1YWI2YjIiLCJzdWIiOiIxNjU3NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMywiZXhwIjoxNjA3NjQ1NzMzfQ.GvBnk3AH1eoCavlIJnd-Xt6g6HNiJHvWB92te_feQiE
```

`GET /api/v1/past_actions`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-11-06 00:15:33 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-12-06 00:15:33 UTC&quot;}
starts_at: 2020-11-06 00:15:33 UTC
ends_at: 2020-12-06 00:15:33 UTC
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "3239",
      "type": "past_actions",
      "attributes": {
        "meeting_id": 7749,
        "compliance_deadline": "2020-11-14T18:15:33.267Z",
        "details_negative": {
          "required_agenda": "This meeting needs an agenda",
          "required_objectives": "An objective is missing. What is the aim of the meeting? Understanding the goal for the meeting helps attendees engage.",
          "last_minute_schedule": "The invitee prefers more time before the meeting starts. A meeting scheduled last second usually means that the meeting could be better prepared.",
          "required_intention": "Missing a intention"
        },
        "organizer_email": null,
        "organizer_notes": null,
        "user_declined": false,
        "user_declined_at": null,
        "action_organizer_warned": true,
        "action_organizer_warned_at": null,
        "action": "reminded",
        "meeting_summary": "Occupy wolf tilde biodiesel yolo vinyl butcher iphone.",
        "meeting_starts_at": "2020-11-15T00:15:33.267Z"
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/past_actions?by_period[starts_at]=2020-11-06+00%3A15%3A33+UTC&by_period[ends_at]=2020-12-06+00%3A15%3A33+UTC&starts_at=2020-11-06+00%3A15%3A33+UTC&ends_at=2020-12-06+00%3A15%3A33+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5NDliYzBhMS01NWYxLTQ1NWYtOTVmMS0zNzU1MDQ1YWI2YjIiLCJzdWIiOiIxNjU3NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMywiZXhwIjoxNjA3NjQ1NzMzfQ.GvBnk3AH1eoCavlIJnd-Xt6g6HNiJHvWB92te_feQiE"
```
# Agenda Items



## Create agenda item


### Request

#### Endpoint

```plaintext
POST /api/v1/meetings/7729/agenda_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzZWQzMGMzNS05NWNmLTQyNTUtOGUwOS1mOGJjM2FmNDY0ZTQiLCJzdWIiOiIxNjQ5MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMSwiZXhwIjoxNjA3NjQ1NzIxfQ.tPklqHcpx4dAJnaoZFrDNupU5yxUOcAK85r6imagT3c
```

`POST /api/v1/meetings/:meeting_id/agenda_items`

#### Parameters


```json
{"data":{"type":"agenda_item","attributes":{"description":"Discuss reticulating the splines.","owner_id":16493,"position":3,"duration_in_mins":15,"started_at":"2020-11-16T00:13:21.018Z"}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| started_at  | The datestamp for when the agenda discussion began |
| duration_in_mins  | Timebox for agenda item |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "4126",
    "type": "agenda_items",
    "attributes": {
      "id": 4126,
      "owner_name": "Hancock Fixer",
      "owner_id": 16493,
      "description": "Discuss reticulating the splines.",
      "duration_in_mins": 15,
      "time_spent_in_secs": null,
      "started_at": "2020-11-16T00:13:21.018Z",
      "ended_at": null,
      "meeting_id": 7729,
      "position": 3
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/7729/agenda_items" -d '{"data":{"type":"agenda_item","attributes":{"description":"Discuss reticulating the splines.","owner_id":16493,"position":3,"duration_in_mins":15,"started_at":"2020-11-16T00:13:21.018Z"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzZWQzMGMzNS05NWNmLTQyNTUtOGUwOS1mOGJjM2FmNDY0ZTQiLCJzdWIiOiIxNjQ5MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMSwiZXhwIjoxNjA3NjQ1NzIxfQ.tPklqHcpx4dAJnaoZFrDNupU5yxUOcAK85r6imagT3c"
```
## Delete agenda item


### Request

#### Endpoint

```plaintext
DELETE /api/v1/meetings/7732/agenda_items/4129
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyMjY0OGQ0OC0xNzdhLTQxZmItOWNhNC1hOWJkMWJjZTIxN2UiLCJzdWIiOiIxNjQ5OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMSwiZXhwIjoxNjA3NjQ1NzIxfQ.QUmXbNOnR-bYZLY5-Kd_Zpgc3Xfm_Sb__sbvRFfxTa0
```

`DELETE /api/v1/meetings/:meeting_id/agenda_items/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| started_at  | The datestamp for when the agenda discussion began |
| duration_in_mins  | Timebox for agenda item |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/meetings/7732/agenda_items/4129" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyMjY0OGQ0OC0xNzdhLTQxZmItOWNhNC1hOWJkMWJjZTIxN2UiLCJzdWIiOiIxNjQ5OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMSwiZXhwIjoxNjA3NjQ1NzIxfQ.QUmXbNOnR-bYZLY5-Kd_Zpgc3Xfm_Sb__sbvRFfxTa0"
```
## List agenda items


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7730/agenda_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3YjlmNmVkYS02NGFhLTQxODAtYWVkYi1hNGQyYjUwOTI1MDIiLCJzdWIiOiIxNjQ5NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMSwiZXhwIjoxNjA3NjQ1NzIxfQ.22Wxyn1g84kzi9MqhctHLPTFcJF6Xj1pLLMLnX6c2eI
```

`GET /api/v1/meetings/:meeting_id/agenda_items`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| started_at  | The datestamp for when the agenda discussion began |
| duration_in_mins  | Timebox for agenda item |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "4127",
      "type": "agenda_items",
      "attributes": {
        "id": 4127,
        "owner_name": "Sasquatch Ivy Clea Strange",
        "owner_id": 16495,
        "description": "Fingerstache try-hard trust fund viral cred loko.",
        "duration_in_mins": 51,
        "time_spent_in_secs": null,
        "started_at": null,
        "ended_at": null,
        "meeting_id": 7730,
        "position": 2
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7730/agenda_items" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3YjlmNmVkYS02NGFhLTQxODAtYWVkYi1hNGQyYjUwOTI1MDIiLCJzdWIiOiIxNjQ5NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMSwiZXhwIjoxNjA3NjQ1NzIxfQ.22Wxyn1g84kzi9MqhctHLPTFcJF6Xj1pLLMLnX6c2eI"
```
## Show agenda item


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7731/agenda_items/4128
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiMGRiODhiOC02MmY5LTRmNGMtOTA0YS05MTYwZjE0ZDQ2ZGYiLCJzdWIiOiIxNjQ5NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMSwiZXhwIjoxNjA3NjQ1NzIxfQ.06SXLKwsE4Pm1EEApGg0qdW6gULBxA765FpsXAzzOrY
```

`GET /api/v1/meetings/:meeting_id/agenda_items/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| started_at  | The datestamp for when the agenda discussion began |
| duration_in_mins  | Timebox for agenda item |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "4128",
    "type": "agenda_items",
    "attributes": {
      "id": 4128,
      "owner_name": "Scorpion Wolf Agent Gorilla Grodd Brain",
      "owner_id": 16497,
      "description": "Master letterpress plaid freegan meh biodiesel photo booth fashion axe.",
      "duration_in_mins": 33,
      "time_spent_in_secs": null,
      "started_at": null,
      "ended_at": null,
      "meeting_id": 7731,
      "position": 2
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7731/agenda_items/4128" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiMGRiODhiOC02MmY5LTRmNGMtOTA0YS05MTYwZjE0ZDQ2ZGYiLCJzdWIiOiIxNjQ5NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMSwiZXhwIjoxNjA3NjQ1NzIxfQ.06SXLKwsE4Pm1EEApGg0qdW6gULBxA765FpsXAzzOrY"
```
## Update agenda item


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/7728/agenda_items/4125
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlOWNiMDFlMS01ODI3LTQ2NTEtOTI2Ni1lMjMwNGI1NTJhMDYiLCJzdWIiOiIxNjQ5MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMCwiZXhwIjoxNjA3NjQ1NzIwfQ.GhjU6PZowpUzrnLwT1zdB95ehd8SWCBGACUbQg2Q0Do
```

`PUT /api/v1/meetings/:meeting_id/agenda_items/:id`

#### Parameters


```json
{"data":{"type":"agenda_item","attributes":{"description":"Talk about things"}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| started_at  | The datestamp for when the agenda discussion began |
| duration_in_mins  | Timebox for agenda item |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "4125",
    "type": "agenda_items",
    "attributes": {
      "id": 4125,
      "owner_name": "Supah Bloodaxe the Fated Captain Cogliostro",
      "owner_id": 16492,
      "description": "Talk about things",
      "duration_in_mins": 16,
      "time_spent_in_secs": null,
      "started_at": null,
      "ended_at": null,
      "meeting_id": 7728,
      "position": 2
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/7728/agenda_items/4125" -d '{"data":{"type":"agenda_item","attributes":{"description":"Talk about things"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlOWNiMDFlMS01ODI3LTQ2NTEtOTI2Ni1lMjMwNGI1NTJhMDYiLCJzdWIiOiIxNjQ5MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMCwiZXhwIjoxNjA3NjQ1NzIwfQ.GhjU6PZowpUzrnLwT1zdB95ehd8SWCBGACUbQg2Q0Do"
```
# Articles



## Create article


### Request

#### Endpoint

```plaintext
POST /api/v1/articles
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2M2MyZDhlMy1mNmE5LTQyMGYtYjRhNi05MTk0YjY5YTUzNWUiLCJzdWIiOiIxNjUzMSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNiwiZXhwIjoxNjA3NjQ1NzI2fQ.ypItyzH_LVjjK5uDhpmocCXPNB4sSdYXpG7Q6A4E1U8
```

`POST /api/v1/articles`

#### Parameters


```json
{"data":{"type":"article","attributes":{"title":"Testing","url":"http://www.meetwell.app","tag_list":"tesing,fun"}}}
```


| Name | Description |
|:-----|:------------|
| tagged_with  | List articles tagged with value |
| not_tagged_with  | List articles not tagged with value |
| order  | Order by column or random |
| title *required* |  title |
| tag_list *required* |  tag list |
| url  |  url |
| pull_quote  |  pull quote |
| publish_on  |  publish on |
| position  |  position |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "323",
    "type": "articles",
    "attributes": {
      "id": 323,
      "title": "Testing",
      "url": "http://www.meetwell.app",
      "pull_quote": null,
      "description": null,
      "position": null,
      "publish_on": "2020-11-16T00:15:26.916Z",
      "tag_list": [
        "tesing",
        "fun"
      ]
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/articles" -d '{"data":{"type":"article","attributes":{"title":"Testing","url":"http://www.meetwell.app","tag_list":"tesing,fun"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2M2MyZDhlMy1mNmE5LTQyMGYtYjRhNi05MTk0YjY5YTUzNWUiLCJzdWIiOiIxNjUzMSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNiwiZXhwIjoxNjA3NjQ1NzI2fQ.ypItyzH_LVjjK5uDhpmocCXPNB4sSdYXpG7Q6A4E1U8"
```
## Delete article


### Request

#### Endpoint

```plaintext
DELETE /api/v1/articles/322
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2MzUzNTljMi05MTllLTQ1NWItOTExOS0yYWYyNTJmNTAwNDEiLCJzdWIiOiIxNjUzMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNiwiZXhwIjoxNjA3NjQ1NzI2fQ.bzDvz4_R1KZ9NVQw6kTg489tk-4hsrWu9wwArUpcUak
```

`DELETE /api/v1/articles/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| tagged_with  | List articles tagged with value |
| not_tagged_with  | List articles not tagged with value |
| order  | Order by column or random |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/articles/322" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2MzUzNTljMi05MTllLTQ1NWItOTExOS0yYWYyNTJmNTAwNDEiLCJzdWIiOiIxNjUzMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNiwiZXhwIjoxNjA3NjQ1NzI2fQ.bzDvz4_R1KZ9NVQw6kTg489tk-4hsrWu9wwArUpcUak"
```
## List articles


### Request

#### Endpoint

```plaintext
GET /api/v1/articles
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkMGFlN2QwMS1kNjNlLTRlNTctOTM4YS02OTBjM2NiNTA5NjIiLCJzdWIiOiIxNjUzMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNywiZXhwIjoxNjA3NjQ1NzI3fQ.mqjGD00-4Kgq1klaGTxBGkiXsR_9lXl7si6IiRdEtz8
```

`GET /api/v1/articles`

#### Parameters



| Name | Description |
|:-----|:------------|
| tagged_with  | List articles tagged with value |
| not_tagged_with  | List articles not tagged with value |
| order  | Order by column or random |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "1",
      "type": "articles",
      "attributes": {
        "id": 1,
        "title": "Maker's Schedule, Manager's Schedule",
        "url": "http://www.paulgraham.com/makersschedule.html",
        "pull_quote": "When you're operating on the maker's schedule, meetings are a disaster. A single meeting can blow a whole afternoon, by breaking it into two pieces each too small to do anything hard in. --Paul Graham",
        "description": null,
        "position": null,
        "publish_on": "2020-11-11T02:15:33.149Z",
        "tag_list": [
          "paul-graham",
          "makers-schedule",
          "defend",
          "focus-block"
        ]
      }
    },
    {
      "id": "2",
      "type": "articles",
      "attributes": {
        "id": 2,
        "title": "Why work doesn't happen at work",
        "url": "https://www.ted.com/talks/jason_fried_why_work_doesn_t_happen_at_work",
        "pull_quote": "At the office, most of the interruptions and distractions that really cause people not to get work done are involuntary. ...[Managers and meetings]  keep interrupting you at the wrong time, while you're actually trying to do something they're paying you to do, they tend to interrupt you. That's kind of bad. --Jason Fried",
        "description": null,
        "position": null,
        "publish_on": "2020-11-11T02:15:33.206Z",
        "tag_list": [
          "defend",
          "focus-block",
          "jason-fried"
        ]
      }
    },
    {
      "id": "3",
      "type": "articles",
      "attributes": {
        "id": 3,
        "title": "Studies show the ideal number of people for a meeting is less than 8.",
        "url": "https://www.forbes.com/sites/victoriafine/2018/04/16/why-you-should-never-invite-more-than-7-people-to-your-meeting/#667f1fcd434c",
        "pull_quote": "You shouldn’t invite more than seven people in a meeting, ever. --Victoria Fine",
        "description": null,
        "position": null,
        "publish_on": "2020-11-11T02:15:33.225Z",
        "tag_list": [
          "max-attendees",
          "victoria-fine"
        ]
      }
    },
    {
      "id": "4",
      "type": "articles",
      "attributes": {
        "id": 4,
        "title": "You can say No: 3 ways to turn down a last-minute meeting request",
        "url": "https://www.themuse.com/advice/you-can-say-no-3-ways-to-turn-down-a-lastminute-meeting-request",
        "pull_quote": "It’s possible to say no to a last-minute meeting and still look like a team player. --Sara McCord",
        "description": null,
        "position": null,
        "publish_on": "2020-11-11T02:15:33.241Z",
        "tag_list": [
          "last-minute",
          "sara-mccord"
        ]
      }
    },
    {
      "id": "324",
      "type": "articles",
      "attributes": {
        "id": 324,
        "title": "Asymmetrical squid celiac.",
        "url": "http://jerde.biz/nickolas_hilll",
        "pull_quote": "Gluten-free crucifix wes anderson occupy humblebrag ugh banjo gastropub truffaut kickstarter pork belly narwhal aesthetic.",
        "description": null,
        "position": null,
        "publish_on": "2020-11-16T00:15:27.037Z",
        "tag_list": [
          "tool-tip",
          "test"
        ]
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/articles" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkMGFlN2QwMS1kNjNlLTRlNTctOTM4YS02OTBjM2NiNTA5NjIiLCJzdWIiOiIxNjUzMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNywiZXhwIjoxNjA3NjQ1NzI3fQ.mqjGD00-4Kgq1klaGTxBGkiXsR_9lXl7si6IiRdEtz8"
```
## Show article


### Request

#### Endpoint

```plaintext
GET /api/v1/articles/320
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MzQzYzA2ZS00NzMyLTQzMjktYTQzMi1hYmVlZWU0N2U3YmEiLCJzdWIiOiIxNjUyOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNiwiZXhwIjoxNjA3NjQ1NzI2fQ.hJ1H2E0LAk9vzq8k08U4zT31iKL0h3VhfzmADdMDy_s
```

`GET /api/v1/articles/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| tagged_with  | List articles tagged with value |
| not_tagged_with  | List articles not tagged with value |
| order  | Order by column or random |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "320",
    "type": "articles",
    "attributes": {
      "id": 320,
      "title": "Ramps yr beard.",
      "url": "http://collier.biz/darius_gottlieb",
      "pull_quote": "Kale chips mixtape slow-carb waistcoat roof shoreditch tofu knausgaard artisan freegan.",
      "description": null,
      "position": null,
      "publish_on": "2020-11-16T00:15:26.489Z",
      "tag_list": [
        "tool-tip",
        "test"
      ]
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/articles/320" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MzQzYzA2ZS00NzMyLTQzMjktYTQzMi1hYmVlZWU0N2U3YmEiLCJzdWIiOiIxNjUyOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNiwiZXhwIjoxNjA3NjQ1NzI2fQ.hJ1H2E0LAk9vzq8k08U4zT31iKL0h3VhfzmADdMDy_s"
```
## Update article


### Request

#### Endpoint

```plaintext
PUT /api/v1/articles/321
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NGQ5NTgwMi05ODdmLTRjZjItOWJlNy03YzVjNzFmMDQwODMiLCJzdWIiOiIxNjUyOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNiwiZXhwIjoxNjA3NjQ1NzI2fQ.B3XFpVHJV1FiNvRHiY_p5riC3ATP-RZInNJWc4JUCOY
```

`PUT /api/v1/articles/:id`

#### Parameters


```json
{"data":{"type":"article","attributes":{"title":"Testing again"}}}
```


| Name | Description |
|:-----|:------------|
| tagged_with  | List articles tagged with value |
| not_tagged_with  | List articles not tagged with value |
| order  | Order by column or random |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "321",
    "type": "articles",
    "attributes": {
      "id": 321,
      "title": "Testing again",
      "url": "http://lowe-schmeler.biz/sarai",
      "pull_quote": "Stumptown next level art party banh mi pop-up chia carry quinoa venmo.",
      "description": null,
      "position": null,
      "publish_on": "2020-11-16T00:15:26.637Z",
      "tag_list": [
        "tool-tip",
        "test"
      ]
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/articles/321" -d '{"data":{"type":"article","attributes":{"title":"Testing again"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NGQ5NTgwMi05ODdmLTRjZjItOWJlNy03YzVjNzFmMDQwODMiLCJzdWIiOiIxNjUyOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNiwiZXhwIjoxNjA3NjQ1NzI2fQ.B3XFpVHJV1FiNvRHiY_p5riC3ATP-RZInNJWc4JUCOY"
```
# Attendees



## Create attendee


### Request

#### Endpoint

```plaintext
POST /api/v1/meetings/7743/attendees
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NDgxMzc1MC1kODNkLTRjMjQtYWY0NC1iY2YxNjg2MzE5MjgiLCJzdWIiOiIxNjUxOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNSwiZXhwIjoxNjA3NjQ1NzI1fQ.hwVFVNJ-dMb-L91Jew7dwIjR53IXMngsiWpnTFvhgqM
```

`POST /api/v1/meetings/:meeting_id/attendees`

#### Parameters


```json
{"data":{"type":"attendee","attributes":{"email":"test@test.com","attendee_name":"Test","status":"confirmed"}}}
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |
| status_ *required* | Actual key is status |
| user_id  |  user |
| attendee_name  |  attendee name |
| role  | organizer, note_taker, subject_matter_expert, stakeholder, decision_maker |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "8257",
    "type": "attendees",
    "attributes": {
      "id": 8257,
      "email": "test@test.com",
      "status": "confirmed",
      "role": null,
      "attendee_name": null
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/7743/attendees" -d '{"data":{"type":"attendee","attributes":{"email":"test@test.com","attendee_name":"Test","status":"confirmed"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NDgxMzc1MC1kODNkLTRjMjQtYWY0NC1iY2YxNjg2MzE5MjgiLCJzdWIiOiIxNjUxOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNSwiZXhwIjoxNjA3NjQ1NzI1fQ.hwVFVNJ-dMb-L91Jew7dwIjR53IXMngsiWpnTFvhgqM"
```
## Delete agenda item


### Request

#### Endpoint

```plaintext
DELETE /api/v1/meetings/7742/attendees/8256
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlNmQyNzEzYS1iMzgzLTQ0MDAtOGQzMi01Y2ViMTJmYWM2MGEiLCJzdWIiOiIxNjUxNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNSwiZXhwIjoxNjA3NjQ1NzI1fQ.edC7urtJpnPSBJNvkL5KQKLVCV8vmJtTt-GYMHsGAwU
```

`DELETE /api/v1/meetings/:meeting_id/attendees/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| email *required* |  email |
| status_ *required* | Actual key is status |
| user_id  |  user |
| attendee_name  |  attendee name |
| role  | organizer, note_taker, subject_matter_expert, stakeholder, decision_maker |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/meetings/7742/attendees/8256" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlNmQyNzEzYS1iMzgzLTQ0MDAtOGQzMi01Y2ViMTJmYWM2MGEiLCJzdWIiOiIxNjUxNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNSwiZXhwIjoxNjA3NjQ1NzI1fQ.edC7urtJpnPSBJNvkL5KQKLVCV8vmJtTt-GYMHsGAwU"
```
## List attendees


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7741/attendees
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NGM1YWI5Yy1iZjA1LTRiZjktYjA3YS1kNmE5YWE0ZTQ4MDIiLCJzdWIiOiIxNjUxNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNCwiZXhwIjoxNjA3NjQ1NzI0fQ.sO0MOEY7UOZy1ZTjKVt9km4_OsWcExrVX7l1vGcBmhY
```

`GET /api/v1/meetings/:meeting_id/attendees`

#### Parameters



| Name | Description |
|:-----|:------------|
| email *required* |  email |
| status_ *required* | Actual key is status |
| user_id  |  user |
| attendee_name  |  attendee name |
| role  | organizer, note_taker, subject_matter_expert, stakeholder, decision_maker |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "8255",
      "type": "attendees",
      "attributes": {
        "id": 8255,
        "email": "eusebia_bartoletti@considine-labadie.name",
        "status": "confirmed",
        "role": "subject_matter_expert",
        "attendee_name": null
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7741/attendees" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NGM1YWI5Yy1iZjA1LTRiZjktYjA3YS1kNmE5YWE0ZTQ4MDIiLCJzdWIiOiIxNjUxNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNCwiZXhwIjoxNjA3NjQ1NzI0fQ.sO0MOEY7UOZy1ZTjKVt9km4_OsWcExrVX7l1vGcBmhY"
```
## Show attendee


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7740/attendees/8254
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiYTMyYWMwYi1mNWQ3LTQ4ODUtYmZhYS1mNzk5ZTgyMjFkZGMiLCJzdWIiOiIxNjUxMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNCwiZXhwIjoxNjA3NjQ1NzI0fQ.bNt2IXmeju8ROUpRVWGu57gl_iJJgQwYI8hnmyH-9_0
```

`GET /api/v1/meetings/:meeting_id/attendees/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| email *required* |  email |
| status_ *required* | Actual key is status |
| user_id  |  user |
| attendee_name  |  attendee name |
| role  | organizer, note_taker, subject_matter_expert, stakeholder, decision_maker |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "8254",
    "type": "attendees",
    "attributes": {
      "id": 8254,
      "email": "herman.anderson@bednar.net",
      "status": "confirmed",
      "role": "subject_matter_expert",
      "attendee_name": null
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7740/attendees/8254" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiYTMyYWMwYi1mNWQ3LTQ4ODUtYmZhYS1mNzk5ZTgyMjFkZGMiLCJzdWIiOiIxNjUxMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNCwiZXhwIjoxNjA3NjQ1NzI0fQ.bNt2IXmeju8ROUpRVWGu57gl_iJJgQwYI8hnmyH-9_0"
```
## Update attendee


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/7739/attendees/8253
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3MzQ4YWM5ZC1hMGRlLTQyM2YtODk2YS02MWRkYWVlZDM5ZGMiLCJzdWIiOiIxNjUxMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNCwiZXhwIjoxNjA3NjQ1NzI0fQ.a-sV0bxVPVg0S2gUj9Wp1Yw__qgj_u6BeCiZ3RhJrsM
```

`PUT /api/v1/meetings/:meeting_id/attendees/:id`

#### Parameters


```json
{"data":{"type":"attendee","attributes":{"attendee_name":"Test 2"}}}
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |
| status_ *required* | Actual key is status |
| user_id  |  user |
| attendee_name  |  attendee name |
| role  | organizer, note_taker, subject_matter_expert, stakeholder, decision_maker |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "8253",
    "type": "attendees",
    "attributes": {
      "id": 8253,
      "email": "kareem@towne.name",
      "status": "confirmed",
      "role": "subject_matter_expert",
      "attendee_name": null
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/7739/attendees/8253" -d '{"data":{"type":"attendee","attributes":{"attendee_name":"Test 2"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3MzQ4YWM5ZC1hMGRlLTQyM2YtODk2YS02MWRkYWVlZDM5ZGMiLCJzdWIiOiIxNjUxMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNCwiZXhwIjoxNjA3NjQ1NzI0fQ.a-sV0bxVPVg0S2gUj9Wp1Yw__qgj_u6BeCiZ3RhJrsM"
```
# Calendars



## List added calendars


### Request

#### Endpoint

```plaintext
GET /api/v1/calendars
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5ODIwYTA3YS1mMmE2LTQzYjQtYmExMS03YThmZDZkMzRlYTkiLCJzdWIiOiIxNjU4MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMywiZXhwIjoxNjA3NjQ1NzMzfQ.X_cCoenRrIDZbybqp12i4afx6YD-1Y4PujFSHet3wmI
```

`GET /api/v1/calendars`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "18991",
      "type": "calendars",
      "attributes": {
        "name": "Buffy Woman",
        "primary": false,
        "source": "google",
        "read_only": false,
        "uuid": "44e916ec-ac57-4565-bc8f-02ed71623923",
        "watching": false
      }
    },
    {
      "id": "18992",
      "type": "calendars",
      "attributes": {
        "name": "Doctor Energy",
        "primary": false,
        "source": "google",
        "read_only": false,
        "uuid": "56d7cde0-0562-427c-a556-deedd500076c",
        "watching": false
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/calendars" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5ODIwYTA3YS1mMmE2LTQzYjQtYmExMS03YThmZDZkMzRlYTkiLCJzdWIiOiIxNjU4MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMywiZXhwIjoxNjA3NjQ1NzMzfQ.X_cCoenRrIDZbybqp12i4afx6YD-1Y4PujFSHet3wmI"
```
# Communication Preferences

Opt-in/out of email communications for non-registered users

## Email Opt In


### Request

#### Endpoint

```plaintext
GET /api/v1/communications/email/opt-in?email=test%40test.com
Content-Type: application/vnd.api+json
```

`GET /api/v1/communications/email/opt-in`

#### Parameters


```json
email: test@test.com
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext
Content-Type: text/plain; charset=utf-8
201 Created
```


```json
 
```



```shell
curl -g "http://localhost:3000/api/v1/communications/email/opt-in?email=test%40test.com" -X GET \
	-H "Content-Type: application/vnd.api+json"
```
## Email Opt Out


### Request

#### Endpoint

```plaintext
GET /api/v1/communications/email/opt-out?email=test%40test.com
Content-Type: application/vnd.api+json
```

`GET /api/v1/communications/email/opt-out`

#### Parameters


```json
email: test@test.com
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext

204 No Content
```




```shell
curl -g "http://localhost:3000/api/v1/communications/email/opt-out?email=test%40test.com" -X GET \
	-H "Content-Type: application/vnd.api+json"
```
## Non-registered email is not opted-out


### Request

#### Endpoint

```plaintext
GET /api/v1/communications/email/opted-out?email=test%40test.com
Content-Type: application/vnd.api+json
```

`GET /api/v1/communications/email/opted-out`

#### Parameters


```json
email: test@test.com
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext
Content-Type: text/plain; charset=utf-8
404 Not Found
```


```json
 
```



```shell
curl -g "http://localhost:3000/api/v1/communications/email/opted-out?email=test%40test.com" -X GET \
	-H "Content-Type: application/vnd.api+json"
```
## Non-registered email is opted-out


### Request

#### Endpoint

```plaintext
GET /api/v1/communications/email/opted-out?email=test%40test.com
Content-Type: application/vnd.api+json
```

`GET /api/v1/communications/email/opted-out`

#### Parameters


```json
email: test@test.com
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext

204 No Content
```




```shell
curl -g "http://localhost:3000/api/v1/communications/email/opted-out?email=test%40test.com" -X GET \
	-H "Content-Type: application/vnd.api+json"
```
## User is registered in system


### Request

#### Endpoint

```plaintext
GET /api/v1/communications/email/opted-out?email=test%40test.com
Content-Type: application/vnd.api+json
```

`GET /api/v1/communications/email/opted-out`

#### Parameters


```json
email: test@test.com
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext

304 Not Modified
```




```shell
curl -g "http://localhost:3000/api/v1/communications/email/opted-out?email=test%40test.com" -X GET \
	-H "Content-Type: application/vnd.api+json"
```
# Goals



## List goals


### Request

#### Endpoint

```plaintext
GET /api/v1/goals
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjMjY0MGZhMy0yZjhmLTRlYjItODdmNS0xZjAzNzU1OTI4ZmQiLCJzdWIiOiIxNjYyMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MCwiZXhwIjoxNjA3NjQ1NzQwfQ.Kg9dh3dZSs3uYs9tLC17lsS7rm37xJuJG5ql1kjfw7U
```

`GET /api/v1/goals`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "11",
      "type": "goals",
      "attributes": {
        "key": "backpack",
        "name": "🎒 Go backpacking",
        "position": null
      }
    },
    {
      "id": "1",
      "type": "goals",
      "attributes": {
        "key": "be_creative",
        "name": "🎨 Be creative",
        "position": null
      }
    },
    {
      "id": "6",
      "type": "goals",
      "attributes": {
        "key": "be_strategic",
        "name": "📆 Be more strategic",
        "position": null
      }
    },
    {
      "id": "8",
      "type": "goals",
      "attributes": {
        "key": "exercise",
        "name": "💪 Exercise",
        "position": null
      }
    },
    {
      "id": "5",
      "type": "goals",
      "attributes": {
        "key": "get_things_done",
        "name": "🖋 Get things done",
        "position": null
      }
    },
    {
      "id": "3",
      "type": "goals",
      "attributes": {
        "key": "hang_with_kids",
        "name": "😎 Hang with the kids",
        "position": null
      }
    },
    {
      "id": "2",
      "type": "goals",
      "attributes": {
        "key": "learn_something",
        "name": "🏄 Learn something new",
        "position": null
      }
    },
    {
      "id": "9",
      "type": "goals",
      "attributes": {
        "key": "meditate",
        "name": "😌 Meditate",
        "position": null
      }
    },
    {
      "id": "10",
      "type": "goals",
      "attributes": {
        "key": "sleep",
        "name": "😪 Sleep",
        "position": null
      }
    },
    {
      "id": "12",
      "type": "goals",
      "attributes": {
        "key": "sports",
        "name": "⚾️ Watch sports",
        "position": null
      }
    },
    {
      "id": "7",
      "type": "goals",
      "attributes": {
        "key": "take_time_off",
        "name": "⏱ Take some time off",
        "position": null
      }
    },
    {
      "id": "4",
      "type": "goals",
      "attributes": {
        "key": "time_with_spouse",
        "name": "😘 Spend time with your partner",
        "position": null
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/goals" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjMjY0MGZhMy0yZjhmLTRlYjItODdmNS0xZjAzNzU1OTI4ZmQiLCJzdWIiOiIxNjYyMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MCwiZXhwIjoxNjA3NjQ1NzQwfQ.Kg9dh3dZSs3uYs9tLC17lsS7rm37xJuJG5ql1kjfw7U"
```
# Google Calendar



## List Google Calendars


### Request

#### Endpoint

```plaintext
GET /api/v1/google_calendar/list
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNWFjOTU0NS0wNWMwLTQ5NzMtYjUxNi1jMGRlYmFlZjVmZjEiLCJzdWIiOiIxNjU2NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMSwiZXhwIjoxNjA3NjQ1NzMxfQ.rl9fL7L-LYRf8hPO0TrgCCZ_Jc07Cjm3wGtOdjju_BI
```

`GET /api/v1/google_calendar/list`

#### Parameters



| Name | Description |
|:-----|:------------|
| show_deleted  | Show deleted Google calendars |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "family08643361170578082544@group.calendar.google.com",
      "type": "external_calendars",
      "attributes": {
        "name": "Family",
        "primary": false,
        "deleted": null
      }
    },
    {
      "id": "6i5saadl27kpd8b7mgg2van2kt_20191030T200000Z",
      "type": "external_calendars",
      "attributes": {
        "name": "Personal",
        "primary": true,
        "deleted": null
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/google_calendar/list" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNWFjOTU0NS0wNWMwLTQ5NzMtYjUxNi1jMGRlYmFlZjVmZjEiLCJzdWIiOiIxNjU2NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMSwiZXhwIjoxNjA3NjQ1NzMxfQ.rl9fL7L-LYRf8hPO0TrgCCZ_Jc07Cjm3wGtOdjju_BI"
```
## Setup Google Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/google_calendar/webhooks_setup
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlZDhhYzg0My1kZjRkLTQzMGMtOTExZi1lMGNiNjgyM2Q2MTMiLCJzdWIiOiIxNjU1MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMCwiZXhwIjoxNjA3NjQ1NzMwfQ.Ro1VBd2HPL6wWcSXNMOqhtLwDqdHnpInSh-FZPNVGbw
```

`POST /api/v1/google_calendar/webhooks_setup`

#### Parameters


```json
{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}
```


| Name | Description |
|:-----|:------------|
| calendar_uuid *required* | Google Calendar UUID |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/google_calendar/webhooks_setup" -d '{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlZDhhYzg0My1kZjRkLTQzMGMtOTExZi1lMGNiNjgyM2Q2MTMiLCJzdWIiOiIxNjU1MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMCwiZXhwIjoxNjA3NjQ1NzMwfQ.Ro1VBd2HPL6wWcSXNMOqhtLwDqdHnpInSh-FZPNVGbw"
```
## Stop Google Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/google_calendar/webhooks_stop
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2N2FiODkyOS04OGE5LTQyZDktYWNjYi00NzU0MzdjZDFlMTMiLCJzdWIiOiIxNjU1NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMCwiZXhwIjoxNjA3NjQ1NzMwfQ.owXnN3-jqNyLHTlEGpJuVeUbAljKaZodFWQFfzss0WA
```

`POST /api/v1/google_calendar/webhooks_stop`

#### Parameters


```json
{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}
```


| Name | Description |
|:-----|:------------|
| calendar_uuid *required* | Google Calendar UUID |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/google_calendar/webhooks_stop" -d '{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2N2FiODkyOS04OGE5LTQyZDktYWNjYi00NzU0MzdjZDFlMTMiLCJzdWIiOiIxNjU1NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMCwiZXhwIjoxNjA3NjQ1NzMwfQ.owXnN3-jqNyLHTlEGpJuVeUbAljKaZodFWQFfzss0WA"
```
## Watch Google Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/google_calendar/events/watch
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1YmY5YzM2YS1hOTEyLTQyOWItYjA3Zi03MzEwY2I4ZWEwNmMiLCJzdWIiOiIxNjU1NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMCwiZXhwIjoxNjA3NjQ1NzMwfQ.LlvhZrsqDUAYDGYy4SXu02lBKFpWH1S_5fCF4i3BwZE
```

`POST /api/v1/google_calendar/events/watch`

#### Parameters


None known.


### Response

```plaintext
Content-Type: text/plain; charset=utf-8
200 OK
```


```json
 
```



```shell
curl "http://localhost:3000/api/v1/google_calendar/events/watch" -d '' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1YmY5YzM2YS1hOTEyLTQyOWItYjA3Zi03MzEwY2I4ZWEwNmMiLCJzdWIiOiIxNjU1NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMCwiZXhwIjoxNjA3NjQ1NzMwfQ.LlvhZrsqDUAYDGYy4SXu02lBKFpWH1S_5fCF4i3BwZE" \
	-H "X-Goog-Channel: 6391fe39-061b-4d83-a5f3-e8279d53826c" \
	-H "X-Goog-Resource: c7e34897-482c-411a-aa5f-75a7ccbec914"
```
# Invoices



## Get invoices


### Request

#### Endpoint

```plaintext
GET /api/v1/invoices
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzY2U2ODU2NC04MGMyLTRhOGMtYjJhZi0zYThkYTNlYzUxZGYiLCJzdWIiOiIxNjUwNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMywiZXhwIjoxNjA3NjQ1NzIzfQ.il0CbEkMGAktUCbaqy2H5PDMZPIqvVRH5HjaSg5Hszc
```

`GET /api/v1/invoices`

#### Parameters



| Name | Description |
|:-----|:------------|
| billing_admin *required* | User must be a billing admin |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [

  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/invoices" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzY2U2ODU2NC04MGMyLTRhOGMtYjJhZi0zYThkYTNlYzUxZGYiLCJzdWIiOiIxNjUwNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMywiZXhwIjoxNjA3NjQ1NzIzfQ.il0CbEkMGAktUCbaqy2H5PDMZPIqvVRH5HjaSg5Hszc"
```
# Meeting Categories



## List meeting categories


### Request

#### Endpoint

```plaintext
GET /api/v1/meeting_categories
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkMDdjNzM2MS1jNzA2LTQ4NzItYWJjYi1iYjhlNjcwMzgwODMiLCJzdWIiOiIxNjQ4MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcxOSwiZXhwIjoxNjA3NjQ1NzE5fQ.OxHbKwOn0AIwijbjWMVkMOmDZM8hwusZ3qUa_MGGhtM
```

`GET /api/v1/meeting_categories`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "4e784a98-a431-40c2-825c-17e1c9e304cf",
    "type": "meeting_categories",
    "attributes": {
      "labels": {
        "recurring": "Recurring",
        "all_hands": "All hands",
        "one_on_one": "One on one",
        "all_day": "All day",
        "unassigned": "Unassigned"
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meeting_categories" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkMDdjNzM2MS1jNzA2LTQ4NzItYWJjYi1iYjhlNjcwMzgwODMiLCJzdWIiOiIxNjQ4MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcxOSwiZXhwIjoxNjA3NjQ1NzE5fQ.OxHbKwOn0AIwijbjWMVkMOmDZM8hwusZ3qUa_MGGhtM"
```
# Meeting Evaluation



## Show meeting evaluation


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7769/evaluation
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxZDE3ZTVlMC03NTVkLTRiZjgtYWY3ZC0wMDA0NjE1ODI0ZmMiLCJzdWIiOiIxNjYzOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MywiZXhwIjoxNjA3NjQ1NzQzfQ.e1IkSJt3R5-1F5FnthKfIggms5g_csFxi7qo8y3RuH8
```

`GET /api/v1/meetings/:meeting_id/evaluation`

#### Parameters



| Name | Description |
|:-----|:------------|
| meeting_id *required* |  meeting |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "7769",
    "type": "meetings",
    "attributes": {
      "summary": "Aesthetic fashion axe scenester asymmetrical disrupt +1 goth.",
      "description": "Voluptatum similique repellat. Ratione voluptatem veritatis. Sunt aut accusamus. Pariatur error ut.",
      "starts_at": "2020-11-16T00:20:43.350Z",
      "ends_at": "2020-11-16T01:20:43.350Z",
      "category_list": [

      ],
      "intention": null,
      "location": "6226 Mitchel Place, West Claytonview, MO 54619",
      "duration": 3600,
      "maybe_focus_block": false,
      "maybe_life_block": false,
      "status": null,
      "edit_permission": true,
      "wellness_block_id": null,
      "event_report_card_id": null,
      "compliance_deadline": "2020-11-15T18:20:43.350Z",
      "wellness_block_category": null,
      "details_negative": {
        "last_minute_schedule": "The invitee prefers more time before the meeting starts. A meeting scheduled last second usually means that the meeting could be better prepared.",
        "required_intention": "Missing a intention"
      },
      "details_positive": {
        "meeting_conflict": "There are no conflicts with any other meetings.",
        "required_agenda": "A time-boxed agenda!",
        "required_objectives": "Nice! Objectives help attendees justify spending their valuable time as well as prepare for and best engage in a meeting.",
        "desired_duration": "This is an acceptable length of time."
      },
      "focus_blockable": false,
      "life_blockable": true,
      "attendees": [
        {
          "email": "dacia@sporer.net",
          "optional": false,
          "domain": "sporer.net",
          "role": "subject_matter_expert"
        }
      ],
      "attendees_count": 1,
      "cost": 38.0,
      "recurring_meeting": false,
      "metadata_importable": null,
      "has_progress": null,
      "score": 68,
      "results": {
        "required_agenda": {
          "points": 25.0,
          "weight": 25.0,
          "score": 100.0
        },
        "meeting_conflict": {
          "points": 20.0,
          "weight": 20.0,
          "score": 100.0
        },
        "required_objectives": {
          "points": 15.000000000000002,
          "weight": 15.000000000000002,
          "score": 100.0
        },
        "desired_duration": {
          "points": 8.5,
          "weight": 10.0,
          "score": 85.0
        },
        "last_minute_schedule": {
          "points": 0.06943411527777812,
          "weight": 20.0,
          "score": 0.34717057638889065
        },
        "required_intention": {
          "points": 0.0,
          "weight": 10.0,
          "score": 0.0
        }
      },
      "quality_label": "Why attend meetings that are below average?",
      "agenda_items": {
        "data": [
          {
            "id": "4139",
            "type": "agenda_items",
            "attributes": {
              "id": 4139,
              "owner_name": "Green Bishop Dragon Moon Knight Fist",
              "owner_id": 16641,
              "description": "Raw denim williamsburg trust fund forage venmo.",
              "duration_in_mins": 69,
              "time_spent_in_secs": null,
              "started_at": null,
              "ended_at": null,
              "meeting_id": 7769,
              "position": 2
            }
          }
        ]
      },
      "objectives": {
        "data": [
          {
            "id": "810",
            "type": "objectives",
            "attributes": {
              "meeting_id": 7769,
              "description": "Crucifix diy asymmetrical loko ennui dreamcatcher disrupt marfa offal messenger bag mixtape.",
              "position": null
            }
          }
        ]
      },
      "prework_items": {
        "data": [
          {
            "id": "621",
            "type": "prework_items",
            "attributes": {
              "id": 621,
              "description": "Offal freegan church-key stumptown whatever selfies pour-over vinyl.",
              "url": "http://price-gusikowski.net/roscoe",
              "timebox": 3600
            }
          }
        ]
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7769/evaluation" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxZDE3ZTVlMC03NTVkLTRiZjgtYWY3ZC0wMDA0NjE1ODI0ZmMiLCJzdWIiOiIxNjYzOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MywiZXhwIjoxNjA3NjQ1NzQzfQ.e1IkSJt3R5-1F5FnthKfIggms5g_csFxi7qo8y3RuH8"
```
## Show meeting progress


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7768/evaluation/progress
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiYjEzZjBjMS03N2U4LTRkMmItODJlMi01NzkxZmYyZWNmOWYiLCJzdWIiOiIxNjYzNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MywiZXhwIjoxNjA3NjQ1NzQzfQ.oEctTp0Cv7ECC5PktL58gyoXTXcNJDNhchoSFr03nwc
```

`GET /api/v1/meetings/:meeting_id/evaluation/progress`

#### Parameters



| Name | Description |
|:-----|:------------|
| meeting_id *required* |  meeting |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "81",
      "type": "meeting_evaluation_versions",
      "attributes": {
        "id": 81,
        "date": "2020-11-16T00:15:43.188Z",
        "score": [
          68,
          88
        ],
        "details_positive": [
          "The number of attendees is acceptable."
        ],
        "details_negative": [

        ]
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7768/evaluation/progress" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiYjEzZjBjMS03N2U4LTRkMmItODJlMi01NzkxZmYyZWNmOWYiLCJzdWIiOiIxNjYzNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MywiZXhwIjoxNjA3NjQ1NzQzfQ.oEctTp0Cv7ECC5PktL58gyoXTXcNJDNhchoSFr03nwc"
```
# Meeting Intentions



## List meeting intentions


### Request

#### Endpoint

```plaintext
GET /api/v1/meeting_intentions
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyNjFhMjZmYy03ZGM4LTQ1ZWYtYThjOC05MGYxODAwYjE5MDEiLCJzdWIiOiIxNjU3OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMywiZXhwIjoxNjA3NjQ1NzMzfQ.eg2L7aRyqYLrUotBuhFplnJOe5dQOqHz7hCzk8BKd3k
```

`GET /api/v1/meeting_intentions`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "df3bb223-b4d2-4dad-abd8-3b0b7ae0c87b",
    "type": "meeting_intentions",
    "attributes": {
      "labels": {
        "standup": "Stand up",
        "planning": "Planning",
        "retrospective": "Retrospective",
        "information": "Info sharing",
        "brainstorming": "Brainstorming",
        "consensus": "Decision Making",
        "kickoff": "Kick-off",
        "teambuilding": "Team building",
        "unassigned": "Unassigned"
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meeting_intentions" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyNjFhMjZmYy03ZGM4LTQ1ZWYtYThjOC05MGYxODAwYjE5MDEiLCJzdWIiOiIxNjU3OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMywiZXhwIjoxNjA3NjQ1NzMzfQ.eg2L7aRyqYLrUotBuhFplnJOe5dQOqHz7hCzk8BKd3k"
```
# Meetings



## Accept a meeting invite


### Request

#### Endpoint

```plaintext
GET /api/v1/users/meetings/accept/7766
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhMGM2OTI5OS1jMjFjLTQwNzItODRjNy02NmNlZGRhNDBkZTkiLCJzdWIiOiIxNjYzMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MiwiZXhwIjoxNjA3NjQ1NzQyfQ.rH64mxHlG2SDurzLZ9cwZkOEhCkzZV6txzCF9_UMJHw
```

`GET /api/v1/users/meetings/accept/:id`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "5473",
    "type": "user_meetings",
    "attributes": {
      "non_compliance_action": null,
      "organizer_notes": null,
      "meeting_id": 7766,
      "user_id": 16630,
      "token": "UHG3W5mJfdieG4rE1dnTBLNQ"
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/users/meetings/accept/7766" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhMGM2OTI5OS1jMjFjLTQwNzItODRjNy02NmNlZGRhNDBkZTkiLCJzdWIiOiIxNjYzMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MiwiZXhwIjoxNjA3NjQ1NzQyfQ.rH64mxHlG2SDurzLZ9cwZkOEhCkzZV6txzCF9_UMJHw"
```
## Convert meeting to focus block


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7753/make_focus_block
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiYWNjMjY3Mi0xZTgzLTQxYmUtYjBmNS04OWQ4ODlhZDU1ZTMiLCJzdWIiOiIxNjU5MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNSwiZXhwIjoxNjA3NjQ1NzM1fQ.S3lBHOZsieCxIgirlCTkFld0NcV-lxxebBZ_JBbbyrI
```

`GET /api/v1/meetings/:id/make_focus_block`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "660",
    "type": "focus_blocks",
    "attributes": {
      "label": "Coding",
      "category": "focus",
      "calendar_id": 19002,
      "recurring_meeting_uuid": "6vkb5i9kqmu36jr1t0v48lkcrk",
      "duration": 3600,
      "starts_at": "2020-11-09T22:03:00.000Z",
      "ends_at": "2020-11-09T23:03:00.000Z",
      "rrule": "RRULE:FREQ=WEEKLY;BYDAY=MO,TU,WE,FR,SA",
      "recurring": true
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7753/make_focus_block" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiYWNjMjY3Mi0xZTgzLTQxYmUtYjBmNS04OWQ4ODlhZDU1ZTMiLCJzdWIiOiIxNjU5MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNSwiZXhwIjoxNjA3NjQ1NzM1fQ.S3lBHOZsieCxIgirlCTkFld0NcV-lxxebBZ_JBbbyrI"
```
## Convert meeting to life block


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7756/make_life_block
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1ZGRhNjlhYy1iNjJiLTQyMTUtYWI2NC05YTA5MGY5OGFhNTkiLCJzdWIiOiIxNjU5OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNywiZXhwIjoxNjA3NjQ1NzM3fQ.083UG6ha1iReJpIZY53hOzMxd3MFPzF_v9CLeDckDXs
```

`GET /api/v1/meetings/:id/make_life_block`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "661",
    "type": "focus_blocks",
    "attributes": {
      "label": "Coding",
      "category": "life",
      "calendar_id": 19011,
      "recurring_meeting_uuid": "6vkb5i9kqmu36jr1t0v48lkcrk",
      "duration": 3600,
      "starts_at": "2020-11-09T22:03:00.000Z",
      "ends_at": "2020-11-09T23:03:00.000Z",
      "rrule": "RRULE:FREQ=WEEKLY;BYDAY=MO,TU,WE,FR,SA",
      "recurring": true
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7756/make_life_block" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1ZGRhNjlhYy1iNjJiLTQyMTUtYWI2NC05YTA5MGY5OGFhNTkiLCJzdWIiOiIxNjU5OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNywiZXhwIjoxNjA3NjQ1NzM3fQ.083UG6ha1iReJpIZY53hOzMxd3MFPzF_v9CLeDckDXs"
```
## Import meeting metadata


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7750/metadata?source_meeting_id=test
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlZGE3NDU2YS0xZWE2LTQxYzctOTVmMC0wZjVjNmE3OTQ5N2MiLCJzdWIiOiIxNjU4MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNCwiZXhwIjoxNjA3NjQ1NzM0fQ.yPVRQkpzqseAiyZZg6ZuzNX_-REbxzW0jpKZBR6jiHA
```

`GET /api/v1/meetings/:id/metadata`

#### Parameters


```json
source_meeting_id: test
```


| Name | Description |
|:-----|:------------|
| import_action  | replace |
| source_meeting_id *required* |  source meeting |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "7750",
    "type": "meetings",
    "attributes": {
      "summary": "Biodiesel celiac you probably haven't heard of them craft beer neutra flannel.",
      "description": "Numquam corrupti voluptas. Expedita tempore sed. Debitis consectetur vel. Beatae pariatur repudiandae.",
      "starts_at": "2020-11-16T00:20:34.248Z",
      "ends_at": "2020-11-16T01:20:34.248Z",
      "category_list": [

      ],
      "intention": null,
      "location": "77920 Taylor Valleys, Lake Pearlene, CO 27643-6597",
      "duration": 3600,
      "maybe_focus_block": false,
      "maybe_life_block": false,
      "status": null,
      "edit_permission": true,
      "wellness_block_id": null,
      "event_report_card_id": null,
      "compliance_deadline": null,
      "wellness_block_category": null,
      "details_negative": null,
      "details_positive": null,
      "focus_blockable": null,
      "life_blockable": null,
      "attendees": [
        {
          "email": "benita.renner@sanford-green.io",
          "optional": false,
          "domain": "sanford-green.io",
          "role": "subject_matter_expert"
        }
      ],
      "attendees_count": 1,
      "cost": null,
      "recurring_meeting": false,
      "metadata_importable": null,
      "has_progress": null,
      "score": null,
      "results": null,
      "quality_label": null,
      "agenda_items": {
        "data": [
          {
            "id": "4130",
            "type": "agenda_items",
            "attributes": {
              "id": 4130,
              "owner_name": "Green Martian Manhunter Box Woman",
              "owner_id": 16584,
              "description": "Knausgaard kitsch street waistcoat hammock kale chips.",
              "duration_in_mins": 23,
              "time_spent_in_secs": null,
              "started_at": null,
              "ended_at": null,
              "meeting_id": 7750,
              "position": 2
            }
          }
        ]
      },
      "objectives": {
        "data": [
          {
            "id": "801",
            "type": "objectives",
            "attributes": {
              "meeting_id": 7750,
              "description": "Bushwick pork belly shabby chic locavore waistcoat meggings poutine cliche kickstarter celiac chicharrones tilde.",
              "position": null
            }
          }
        ]
      },
      "prework_items": {
        "data": [
          {
            "id": "606",
            "type": "prework_items",
            "attributes": {
              "id": 606,
              "description": "Post-ironic distillery try-hard raw denim vinegar.",
              "url": "http://crona.com/gwen_macgyver",
              "timebox": 3600
            }
          },
          {
            "id": "608",
            "type": "prework_items",
            "attributes": {
              "id": 608,
              "description": "Post-ironic distillery try-hard raw denim vinegar.",
              "url": "http://crona.com/gwen_macgyver",
              "timebox": 3600
            }
          }
        ]
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7750/metadata?source_meeting_id=test" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlZGE3NDU2YS0xZWE2LTQxYzctOTVmMC0wZjVjNmE3OTQ5N2MiLCJzdWIiOiIxNjU4MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNCwiZXhwIjoxNjA3NjQ1NzM0fQ.yPVRQkpzqseAiyZZg6ZuzNX_-REbxzW0jpKZBR6jiHA"
```
## List meetings


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings?by_period[starts_at]=2020-11-16+00%3A15%3A37+UTC&amp;by_period[ends_at]=2020-11-23+00%3A15%3A37+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkODQ1MjYzYi0zZTVhLTQ5MDMtOTQ2Mi00ZmM2OGQ1Mjc2MTAiLCJzdWIiOiIxNjYwMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNywiZXhwIjoxNjA3NjQ1NzM3fQ.h_Kk0Tfw4Of6YRW1Fvo6AwtUj5FNMsninbxrAllmVtw
```

`GET /api/v1/meetings`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-11-16 00:15:37 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-23 00:15:37 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "7757",
      "type": "meetings",
      "attributes": {
        "summary": "Umami skateboard bicycle rights cornhole xoxo.",
        "description": "Suscipit minus ut. Culpa consequatur qui. Rerum explicabo beatae. Sit aut voluptas.",
        "starts_at": "2020-11-16T00:20:37.504Z",
        "ends_at": "2020-11-16T01:20:37.504Z",
        "category_list": [

        ],
        "location": "962 Reynolds Views, Winfordville, CT 76111",
        "duration": 3600,
        "status": null,
        "wellness_block_id": null,
        "wellness_block_category": null,
        "event_report_card_id": null,
        "score": null,
        "recurring_meeting": false,
        "agenda_items": {
          "data": [

          ]
        },
        "objectives": {
          "data": [

          ]
        },
        "prework_items": {
          "data": [

          ]
        }
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings?by_period[starts_at]=2020-11-16+00%3A15%3A37+UTC&by_period[ends_at]=2020-11-23+00%3A15%3A37+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkODQ1MjYzYi0zZTVhLTQ5MDMtOTQ2Mi00ZmM2OGQ1Mjc2MTAiLCJzdWIiOiIxNjYwMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNywiZXhwIjoxNjA3NjQ1NzM3fQ.h_Kk0Tfw4Of6YRW1Fvo6AwtUj5FNMsninbxrAllmVtw"
```
## Meeting details for unauthenticated organizer


### Request

#### Endpoint

```plaintext
GET /api/v1/users/meetings/details/Ejt7GxLRhXqWj9Mf6u3ZT8J2
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2ZmY5YjczOC04NzIyLTQ2NzYtYjZjOC03NGI3ODYyNTg4MGIiLCJzdWIiOiIxNjYyNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MSwiZXhwIjoxNjA3NjQ1NzQxfQ.YiBNyE_KYNkWZAlrJWPJ9RWW1mpxpL5r1MlBGHRIwLo
```

`GET /api/v1/users/meetings/details/:user_meeting_token`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "7765",
    "type": "meetings",
    "attributes": {
      "summary": "8-bit food truck waistcoat 90's post-ironic.",
      "description": "Eum occaecati est. Est ad qui. Consequatur ea fugit. Dolorem est eius.",
      "starts_at": "2020-11-16T00:20:41.332Z",
      "ends_at": "2020-11-16T01:20:41.332Z",
      "category_list": [

      ],
      "intention": null,
      "location": "Suite 568 52978 Konopelski Vista, Shanahanside, TX 87853-7860",
      "duration": 3600,
      "maybe_focus_block": false,
      "maybe_life_block": false,
      "status": null,
      "edit_permission": true,
      "wellness_block_id": null,
      "event_report_card_id": null,
      "compliance_deadline": "2020-11-15T18:20:41.332Z",
      "wellness_block_category": null,
      "details_negative": {
        "required_agenda": "This meeting needs an agenda",
        "required_objectives": "An objective is missing. What is the aim of the meeting? Understanding the goal for the meeting helps attendees engage.",
        "last_minute_schedule": "The invitee prefers more time before the meeting starts. A meeting scheduled last second usually means that the meeting could be better prepared.",
        "required_intention": "Missing a intention"
      },
      "details_positive": {
        "meeting_conflict": "There are no conflicts with any other meetings.",
        "max_attendees": "The number of attendees is acceptable.",
        "desired_duration": "This is an acceptable length of time."
      },
      "focus_blockable": false,
      "life_blockable": true,
      "attendees": [
        {
          "email": "shantay@rau.name",
          "optional": false,
          "domain": "rau.name",
          "role": "subject_matter_expert"
        },
        {
          "email": "ariana_goyette@stehr.net",
          "optional": false,
          "domain": "stehr.net",
          "role": "subject_matter_expert"
        }
      ],
      "attendees_count": 2,
      "cost": 76.0,
      "recurring_meeting": false,
      "metadata_importable": null,
      "has_progress": null,
      "score": 34,
      "results": null,
      "quality_label": "An F? Is that what you feel your time is worth?",
      "agenda_items": {
        "data": [

        ]
      },
      "objectives": {
        "data": [

        ]
      },
      "prework_items": {
        "data": [

        ]
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/users/meetings/details/Ejt7GxLRhXqWj9Mf6u3ZT8J2" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2ZmY5YjczOC04NzIyLTQ2NzYtYjZjOC03NGI3ODYyNTg4MGIiLCJzdWIiOiIxNjYyNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MSwiZXhwIjoxNjA3NjQ1NzQxfQ.YiBNyE_KYNkWZAlrJWPJ9RWW1mpxpL5r1MlBGHRIwLo"
```
## Organizer prevents a decline


### Request

#### Endpoint

```plaintext
PUT /api/v1/users/meetings/prevent_decline/6cnbXeV12DaoLF8TQpt463tu
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4Y2JhYmQyMy0xMThkLTQyODQtOGIzYy0xODI2MjMzMjdlYzciLCJzdWIiOiIxNjYyMSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MCwiZXhwIjoxNjA3NjQ1NzQwfQ.Y-6fk8IkUzSezo9bm_yf5gPeMgjrWAiIxpULHjPGU_Y
```

`PUT /api/v1/users/meetings/prevent_decline/:user_meeting_token`

#### Parameters


```json
{"data":{"type":"user_meeting","attributes":{"organizer_notes":"Testing!"}}}
```

None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "5470",
    "type": "user_meetings",
    "attributes": {
      "non_compliance_action": "do nothing",
      "organizer_notes": "Testing!",
      "meeting_id": 7763,
      "user_id": 16621,
      "token": "6cnbXeV12DaoLF8TQpt463tu"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/users/meetings/prevent_decline/6cnbXeV12DaoLF8TQpt463tu" -d '{"data":{"type":"user_meeting","attributes":{"organizer_notes":"Testing!"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4Y2JhYmQyMy0xMThkLTQyODQtOGIzYy0xODI2MjMzMjdlYzciLCJzdWIiOiIxNjYyMSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MCwiZXhwIjoxNjA3NjQ1NzQwfQ.Y-6fk8IkUzSezo9bm_yf5gPeMgjrWAiIxpULHjPGU_Y"
```
## Show meeting


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7755
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhMjkxNTg3Zi0xYzRlLTQ4NTYtODY2Ni1mZjY2MjIzNmE3ODAiLCJzdWIiOiIxNjU5NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNiwiZXhwIjoxNjA3NjQ1NzM2fQ.s-Zf96E7Hy-kVARCkUCTasmaGbcbrABO5Vx_w9eoi_M
```

`GET /api/v1/meetings/:id`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "7755",
    "type": "meetings",
    "attributes": {
      "summary": "Knausgaard cliche fingerstache.",
      "description": "Officiis molestiae accusantium. Mollitia in sunt. Amet ut in. Consequatur labore eius.",
      "starts_at": "2020-11-16T00:20:36.566Z",
      "ends_at": "2020-11-16T01:20:36.566Z",
      "category_list": [

      ],
      "intention": null,
      "location": "Apt. 906 63086 Eliseo Summit, Lake Wyattton, OK 62532-3602",
      "duration": 3600,
      "maybe_focus_block": false,
      "maybe_life_block": false,
      "status": null,
      "edit_permission": true,
      "wellness_block_id": null,
      "event_report_card_id": null,
      "compliance_deadline": null,
      "wellness_block_category": null,
      "details_negative": null,
      "details_positive": null,
      "focus_blockable": null,
      "life_blockable": null,
      "attendees": [
        {
          "email": "cyril@roob.org",
          "optional": false,
          "domain": "roob.org",
          "role": "subject_matter_expert"
        }
      ],
      "attendees_count": 1,
      "cost": null,
      "recurring_meeting": false,
      "metadata_importable": null,
      "has_progress": null,
      "score": null,
      "results": null,
      "quality_label": null,
      "agenda_items": {
        "data": [
          {
            "id": "4135",
            "type": "agenda_items",
            "attributes": {
              "id": 4135,
              "owner_name": "Green She-Hulk She-Hulk Spirit",
              "owner_id": 16598,
              "description": "Bespoke green juice kitsch thundercats tacos.",
              "duration_in_mins": 69,
              "time_spent_in_secs": null,
              "started_at": null,
              "ended_at": null,
              "meeting_id": 7755,
              "position": 2
            }
          }
        ]
      },
      "objectives": {
        "data": [
          {
            "id": "806",
            "type": "objectives",
            "attributes": {
              "meeting_id": 7755,
              "description": "Artisan mustache heirloom migas meh crucifix shoreditch chillwave church-key bitters cliche beard.",
              "position": null
            }
          }
        ]
      },
      "prework_items": {
        "data": [
          {
            "id": "612",
            "type": "prework_items",
            "attributes": {
              "id": 612,
              "description": "Humblebrag heirloom kale chips gastropub muggle magic +1 8-bit.",
              "url": "http://ernser.net/tegan.spencer",
              "timebox": 3600
            }
          }
        ]
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7755" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhMjkxNTg3Zi0xYzRlLTQ4NTYtODY2Ni1mZjY2MjIzNmE3ODAiLCJzdWIiOiIxNjU5NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNiwiZXhwIjoxNjA3NjQ1NzM2fQ.s-Zf96E7Hy-kVARCkUCTasmaGbcbrABO5Vx_w9eoi_M"
```
## Show user meeting


### Request

#### Endpoint

```plaintext
GET /api/v1/users/meetings/7764
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNzJlNGYzZS1jMDUyLTRlZDEtYmEyYS04ODFmNGE3NjFlODUiLCJzdWIiOiIxNjYyNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MSwiZXhwIjoxNjA3NjQ1NzQxfQ.W-hDGxjqNAoHagVZplyJVzxYc-ETTd7vTe8g8UwffdM
```

`GET /api/v1/users/meetings/:id`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "5471",
    "type": "user_meetings",
    "attributes": {
      "non_compliance_action": null,
      "organizer_notes": null,
      "meeting_id": 7764,
      "user_id": 16624,
      "token": "bqyHZ1MQNnfv2hN4LxnyiQUe"
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/users/meetings/7764" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNzJlNGYzZS1jMDUyLTRlZDEtYmEyYS04ODFmNGE3NjFlODUiLCJzdWIiOiIxNjYyNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MSwiZXhwIjoxNjA3NjQ1NzQxfQ.W-hDGxjqNAoHagVZplyJVzxYc-ETTd7vTe8g8UwffdM"
```
## Sync meetings for daterange


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/sync?by_period[starts_at]=2020-11-16+00%3A15%3A35+UTC&amp;by_period[ends_at]=2020-11-23+00%3A15%3A35+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3NjA3NjM1Yy1iNDgzLTQ3YmItYjdiYy1iMzNiYzIxNmJiM2QiLCJzdWIiOiIxNjU4NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNSwiZXhwIjoxNjA3NjQ1NzM1fQ.gt0knRz686_ZMuVcAKIE4K8FwbsRYkJH0Hesy3U_rPM
```

`GET /api/v1/meetings/sync`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-11-16 00:15:35 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-23 00:15:35 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "9c8287ca-6ef1-44d1-b67f-8ced8354f5f5",
    "type": "notices",
    "attributes": {
      "message": "Re-evaluating your meetings can take several minutes. Are you sure you want to continue?",
      "meta": {
        "button": "Yes, start a sync",
        "can_sync": true
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/sync?by_period[starts_at]=2020-11-16+00%3A15%3A35+UTC&by_period[ends_at]=2020-11-23+00%3A15%3A35+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3NjA3NjM1Yy1iNDgzLTQ3YmItYjdiYy1iMzNiYzIxNmJiM2QiLCJzdWIiOiIxNjU4NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNSwiZXhwIjoxNjA3NjQ1NzM1fQ.gt0knRz686_ZMuVcAKIE4K8FwbsRYkJH0Hesy3U_rPM"
```
## Update meeting


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/7754
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyY2RiMTE4Ni01NGU2LTRmNDQtYTVjNC04NDA4YTQyNDJmOWUiLCJzdWIiOiIxNjU5MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNiwiZXhwIjoxNjA3NjQ1NzM2fQ.GcfvCDJr2gAAGGWVww_v-0INsuw50Gjr9qifJQi1IdE
```

`PUT /api/v1/meetings/:id`

#### Parameters


```json
{"data":{"type":"agenda_item","attributes":{"started_at":"2020-11-15T23:55:36.378Z","ended_at":"2020-11-16T00:15:36.378Z"}}}
```


| Name | Description |
|:-----|:------------|
| started_at  |  started at |
| ended_at  |  ended at |
| time_spent_in_secs  |  time spent in secs |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "7754",
    "type": "meetings",
    "attributes": {
      "summary": "Yolo drinking tacos humblebrag viral squid.",
      "description": "Necessitatibus accusamus debitis. Consequatur quidem nisi. Quo maxime voluptatem. Odit voluptate facere.",
      "starts_at": "2020-11-16T00:20:36.060Z",
      "ends_at": "2020-11-16T01:20:36.060Z",
      "category_list": [

      ],
      "intention": null,
      "location": "Suite 372 378 McKenzie Estate, Lake Florentinoton, AR 84988-3693",
      "duration": 3600,
      "maybe_focus_block": false,
      "maybe_life_block": false,
      "status": null,
      "edit_permission": true,
      "wellness_block_id": null,
      "event_report_card_id": null,
      "compliance_deadline": null,
      "wellness_block_category": null,
      "details_negative": null,
      "details_positive": null,
      "focus_blockable": false,
      "life_blockable": true,
      "attendees": [
        {
          "email": "devon@jakubowski-sanford.io",
          "optional": false,
          "domain": "jakubowski-sanford.io",
          "role": "subject_matter_expert"
        }
      ],
      "attendees_count": 1,
      "cost": 38.0,
      "recurring_meeting": false,
      "metadata_importable": null,
      "has_progress": null,
      "score": null,
      "results": null,
      "quality_label": null,
      "agenda_items": {
        "data": [
          {
            "id": "4134",
            "type": "agenda_items",
            "attributes": {
              "id": 4134,
              "owner_name": "Gog Magog",
              "owner_id": 16595,
              "description": "Pickled bicycle rights disrupt church-key mlkshk raw denim try-hard tofu.",
              "duration_in_mins": 13,
              "time_spent_in_secs": null,
              "started_at": null,
              "ended_at": null,
              "meeting_id": 7754,
              "position": 2
            }
          }
        ]
      },
      "objectives": {
        "data": [
          {
            "id": "805",
            "type": "objectives",
            "attributes": {
              "meeting_id": 7754,
              "description": "Iphone organic swag brooklyn truffaut selvage 8-bit fingerstache retro tacos chartreuse.",
              "position": null
            }
          }
        ]
      },
      "prework_items": {
        "data": [
          {
            "id": "611",
            "type": "prework_items",
            "attributes": {
              "id": 611,
              "description": "Tousled 90's fingerstache yuccie twee.",
              "url": "http://johns-kiehn.co/velia",
              "timebox": 3600
            }
          }
        ]
      }
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/7754" -d '{"data":{"type":"agenda_item","attributes":{"started_at":"2020-11-15T23:55:36.378Z","ended_at":"2020-11-16T00:15:36.378Z"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyY2RiMTE4Ni01NGU2LTRmNDQtYTVjNC04NDA4YTQyNDJmOWUiLCJzdWIiOiIxNjU5MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNiwiZXhwIjoxNjA3NjQ1NzM2fQ.GcfvCDJr2gAAGGWVww_v-0INsuw50Gjr9qifJQi1IdE"
```
## Update user meeting


### Request

#### Endpoint

```plaintext
PUT /api/v1/users/meetings/7767
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4ZTNjODY0Yi1mMjg0LTQ5ZGYtODQwZS1jOTU3NjgwNDdlMGQiLCJzdWIiOiIxNjYzMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MiwiZXhwIjoxNjA3NjQ1NzQyfQ.ZgrW6MW-FKYf3Re8b1XVXwh2EE3ulyqVIvZLalRP0SM
```

`PUT /api/v1/users/meetings/:id`

#### Parameters


```json
{"data":{"type":"user_meeting","attributes":{"non_compliance_action":"decline"}}}
```


| Name | Description |
|:-----|:------------|
| non_compliance_action *required* | remind, decline, etc |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "5474",
    "type": "user_meetings",
    "attributes": {
      "non_compliance_action": "decline",
      "organizer_notes": null,
      "meeting_id": 7767,
      "user_id": 16633,
      "token": "o3erR7zHEkEcFGqwnKEoBRA7"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/users/meetings/7767" -d '{"data":{"type":"user_meeting","attributes":{"non_compliance_action":"decline"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4ZTNjODY0Yi1mMjg0LTQ5ZGYtODQwZS1jOTU3NjgwNDdlMGQiLCJzdWIiOiIxNjYzMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MiwiZXhwIjoxNjA3NjQ1NzQyfQ.ZgrW6MW-FKYf3Re8b1XVXwh2EE3ulyqVIvZLalRP0SM"
```
# Microsoft Outlook



## List Outlook Calendars


### Request

#### Endpoint

```plaintext
GET /api/v1/microsoft_outlook/list
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0YWZiNzNjNC02ZmIwLTRiYWEtODg0Mi01MzQ3YjI2NjJkNmYiLCJzdWIiOiIxNjU3MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMiwiZXhwIjoxNjA3NjQ1NzMyfQ.ZfnEgk80PgTq7-VX4xkHOvkLRdzyozuesrAXTMaqXEs
```

`GET /api/v1/microsoft_outlook/list`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "AQMkADAwATM0MDAAMS0yMWI4LWMzYTktMDACLTAwCgBGAAAD05FBgSzQMkOHu1sf5cDnwAcAduHsdxvLcUmEsBp_QJ5q8gAAAgEGAAAAduHsdxvLcUmEsBp_QJ5q8gAAAmhcAAAA",
      "type": "external_calendars",
      "attributes": {
        "name": "Calendar",
        "primary": true,
        "deleted": null
      }
    },
    {
      "id": "AQMkADAwATM0MDAAMS0yMWI4LWMzYTktMDACLTAwCgBGAAAD05FBgSzQMkOHu1sf5cDnwAcAduHsdxvLcUmEsBp_QJ5q8gAAAgEGAAAAduHsdxvLcUmEsBp_QJ5q8gAAAmhhAAAA",
      "type": "external_calendars",
      "attributes": {
        "name": "United States holidays",
        "primary": false,
        "deleted": null
      }
    },
    {
      "id": "AQMkADAwATM0MDAAMS0yMWI4LWMzYTktMDACLTAwCgBGAAAD05FBgSzQMkOHu1sf5cDnwAcAduHsdxvLcUmEsBp_QJ5q8gAAAgEGAAAAduHsdxvLcUmEsBp_QJ5q8gAAAmhiAAAA",
      "type": "external_calendars",
      "attributes": {
        "name": "Birthdays",
        "primary": false,
        "deleted": null
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/microsoft_outlook/list" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0YWZiNzNjNC02ZmIwLTRiYWEtODg0Mi01MzQ3YjI2NjJkNmYiLCJzdWIiOiIxNjU3MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMiwiZXhwIjoxNjA3NjQ1NzMyfQ.ZfnEgk80PgTq7-VX4xkHOvkLRdzyozuesrAXTMaqXEs"
```
## Setup Outlook Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/microsoft_outlook/webhooks_setup
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNGQ2ZWIzMy05MGU2LTQ3NWItOWVlNy1lOWI4NmZhMzYzY2QiLCJzdWIiOiIxNjU2NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMiwiZXhwIjoxNjA3NjQ1NzMyfQ.9VDqCe1iiuZIJCSZcOfA34EQA5G_iyv05q6LeEZLJ14
```

`POST /api/v1/microsoft_outlook/webhooks_setup`

#### Parameters


```json
{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}
```


| Name | Description |
|:-----|:------------|
| calendar_uuid *required* | Outlook Calendar UUID |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/microsoft_outlook/webhooks_setup" -d '{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNGQ2ZWIzMy05MGU2LTQ3NWItOWVlNy1lOWI4NmZhMzYzY2QiLCJzdWIiOiIxNjU2NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMiwiZXhwIjoxNjA3NjQ1NzMyfQ.9VDqCe1iiuZIJCSZcOfA34EQA5G_iyv05q6LeEZLJ14"
```
## Stop Outlook Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/microsoft_outlook/webhooks_stop
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0MDBhNWYzZC1kMjhhLTQyZGItODY3MC03NTQ4YzBjOTJlMTQiLCJzdWIiOiIxNjU3MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMiwiZXhwIjoxNjA3NjQ1NzMyfQ.lG_1Hds3P1TRFZqkFOQTq_LXdyEbvEomb2bEVWptbLA
```

`POST /api/v1/microsoft_outlook/webhooks_stop`

#### Parameters


```json
{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}
```


| Name | Description |
|:-----|:------------|
| calendar_uuid *required* | Outlook Calendar UUID |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/microsoft_outlook/webhooks_stop" -d '{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0MDBhNWYzZC1kMjhhLTQyZGItODY3MC03NTQ4YzBjOTJlMTQiLCJzdWIiOiIxNjU3MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMiwiZXhwIjoxNjA3NjQ1NzMyfQ.lG_1Hds3P1TRFZqkFOQTq_LXdyEbvEomb2bEVWptbLA"
```
## Watch Outlook Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/microsoft_outlook/events/watch
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1N2M4ZTlkYy00NTVkLTRhZGYtOWIzNy03NzFiNmM0YzYwNjkiLCJzdWIiOiIxNjU2OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMiwiZXhwIjoxNjA3NjQ1NzMyfQ.SF0QaSHSxjLJsIOvdaRxH7_8LF0G93w55nLEDg4YAoU
```

`POST /api/v1/microsoft_outlook/events/watch`

#### Parameters


```json
{"value":[{"clientState":"ab6d4fd4-a529-431c-b746-63795db96c13","subscriptionId":"35c89222-0741-4687-933e-6be522f4107f"}]}
```


| Name | Description |
|:-----|:------------|
| value *required* |  value |



### Response

```plaintext
Content-Type: text/plain; charset=utf-8
202 Accepted
```


```json
 
```



```shell
curl "http://localhost:3000/api/v1/microsoft_outlook/events/watch" -d '{"value":[{"clientState":"ab6d4fd4-a529-431c-b746-63795db96c13","subscriptionId":"35c89222-0741-4687-933e-6be522f4107f"}]}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1N2M4ZTlkYy00NTVkLTRhZGYtOWIzNy03NzFiNmM0YzYwNjkiLCJzdWIiOiIxNjU2OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMiwiZXhwIjoxNjA3NjQ1NzMyfQ.SF0QaSHSxjLJsIOvdaRxH7_8LF0G93w55nLEDg4YAoU"
```
## Watch Outlook Webhook Lifecycle


### Request

#### Endpoint

```plaintext
POST /api/v1/microsoft_outlook/events/lifecycle
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjNThhNmUzMC0wOGUzLTQzZmEtOWY4MS03NWMxZDc0NzJiMDUiLCJzdWIiOiIxNjU2NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMSwiZXhwIjoxNjA3NjQ1NzMxfQ.LFhYd6wm8rVy5ILeBowXG32qLESOV5-eh43oVxppLMw
```

`POST /api/v1/microsoft_outlook/events/lifecycle`

#### Parameters


```json
{"value":[{"clientState":"0d2f3e71-c900-4a6a-a420-2ab1fe1237a4","subscriptionId":"04ec79de-35e2-427a-b34c-9369ae0893f1"}]}
```


| Name | Description |
|:-----|:------------|
| validationToken  | Validation Token |
| value *required* |  value |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/microsoft_outlook/events/lifecycle" -d '{"value":[{"clientState":"0d2f3e71-c900-4a6a-a420-2ab1fe1237a4","subscriptionId":"04ec79de-35e2-427a-b34c-9369ae0893f1"}]}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjNThhNmUzMC0wOGUzLTQzZmEtOWY4MS03NWMxZDc0NzJiMDUiLCJzdWIiOiIxNjU2NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMSwiZXhwIjoxNjA3NjQ1NzMxfQ.LFhYd6wm8rVy5ILeBowXG32qLESOV5-eh43oVxppLMw"
```
# Objectives



## Create objective


### Request

#### Endpoint

```plaintext
POST /api/v1/meetings/7733/objectives
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4ODM3Nzk2MS05MDA2LTRlZjItODViNy00OTQ1ODRjZWNiYzkiLCJzdWIiOiIxNjUwMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMiwiZXhwIjoxNjA3NjQ1NzIyfQ.N4X2yWKG_STVfggiCLscnvzAwPpvymOCn-W8IOnu0mY
```

`POST /api/v1/meetings/:meeting_id/objectives`

#### Parameters


```json
{"data":{"type":"objective","attributes":{"description":"Figure something out","position":3}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "796",
    "type": "objectives",
    "attributes": {
      "meeting_id": 7733,
      "description": "Figure something out",
      "position": 3
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/7733/objectives" -d '{"data":{"type":"objective","attributes":{"description":"Figure something out","position":3}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4ODM3Nzk2MS05MDA2LTRlZjItODViNy00OTQ1ODRjZWNiYzkiLCJzdWIiOiIxNjUwMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMiwiZXhwIjoxNjA3NjQ1NzIyfQ.N4X2yWKG_STVfggiCLscnvzAwPpvymOCn-W8IOnu0mY"
```
## Delete objective


### Request

#### Endpoint

```plaintext
DELETE /api/v1/meetings/7737/objectives/800
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5MDMzZmExZi1lZWQ2LTQ2ODItOTlhNy0yODI2NTkwMTQzMDkiLCJzdWIiOiIxNjUwNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMywiZXhwIjoxNjA3NjQ1NzIzfQ.VIKpYPTHZQPjnosMtZVFXJBVYYahpdPuibO0ghNjeg4
```

`DELETE /api/v1/meetings/:meeting_id/objectives/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/meetings/7737/objectives/800" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5MDMzZmExZi1lZWQ2LTQ2ODItOTlhNy0yODI2NTkwMTQzMDkiLCJzdWIiOiIxNjUwNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMywiZXhwIjoxNjA3NjQ1NzIzfQ.VIKpYPTHZQPjnosMtZVFXJBVYYahpdPuibO0ghNjeg4"
```
## List objectives


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7734/objectives
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwNzE0NjBmOS0zYTRkLTQ5MzctYjFmNy0zMWJkYzJhYzU5ODEiLCJzdWIiOiIxNjUwMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMiwiZXhwIjoxNjA3NjQ1NzIyfQ.FDPr0yaE77Y_d2ncO3Wt5z7BX-VWIGVccwkiV3cBSNI
```

`GET /api/v1/meetings/:meeting_id/objectives`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "797",
      "type": "objectives",
      "attributes": {
        "meeting_id": 7734,
        "description": "Waistcoat shabby chic williamsburg deep v artisan sartorial ethical.",
        "position": null
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7734/objectives" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwNzE0NjBmOS0zYTRkLTQ5MzctYjFmNy0zMWJkYzJhYzU5ODEiLCJzdWIiOiIxNjUwMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMiwiZXhwIjoxNjA3NjQ1NzIyfQ.FDPr0yaE77Y_d2ncO3Wt5z7BX-VWIGVccwkiV3cBSNI"
```
## Show objective


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7736/objectives/799
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NmIwMDU5NC0yN2QxLTQ0OGMtOTdlZi1mYzFjMjJhYzFlNzkiLCJzdWIiOiIxNjUwNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMywiZXhwIjoxNjA3NjQ1NzIzfQ.QzgxjyZqYpmjX8clurW9ZIdUlD7U2McYmbVr93mBw0A
```

`GET /api/v1/meetings/:meeting_id/objectives/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "799",
    "type": "objectives",
    "attributes": {
      "meeting_id": 7736,
      "description": "Lomo lo-fi vegan slow-carb mlkshk humblebrag 90's sriracha brunch venmo.",
      "position": null
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7736/objectives/799" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NmIwMDU5NC0yN2QxLTQ0OGMtOTdlZi1mYzFjMjJhYzFlNzkiLCJzdWIiOiIxNjUwNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMywiZXhwIjoxNjA3NjQ1NzIzfQ.QzgxjyZqYpmjX8clurW9ZIdUlD7U2McYmbVr93mBw0A"
```
## Update objective


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/7735/objectives/798
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjN2I5ZDE0NC02ZTM5LTQyMjAtODUyNy1iZDQ4OWNmNzEzYmYiLCJzdWIiOiIxNjUwNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMiwiZXhwIjoxNjA3NjQ1NzIyfQ.UT9CqPGX9MKXwkvYSlFg66ZzHkSIn7NPoBa7OJIwjCc
```

`PUT /api/v1/meetings/:meeting_id/objectives/:id`

#### Parameters


```json
{"data":{"type":"objective","attributes":{"description":"Figure it all out"}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "798",
    "type": "objectives",
    "attributes": {
      "meeting_id": 7735,
      "description": "Figure it all out",
      "position": null
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/7735/objectives/798" -d '{"data":{"type":"objective","attributes":{"description":"Figure it all out"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjN2I5ZDE0NC02ZTM5LTQyMjAtODUyNy1iZDQ4OWNmNzEzYmYiLCJzdWIiOiIxNjUwNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMiwiZXhwIjoxNjA3NjQ1NzIyfQ.UT9CqPGX9MKXwkvYSlFg66ZzHkSIn7NPoBa7OJIwjCc"
```
# Organizer Deny-List

Organizers who are denied actions from being performed on them

## Bulk create deny-list entries for company


### Request

#### Endpoint

```plaintext
POST /api/v1/company/denylisted_organizers/bulk
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NDNmMWJlOC0wMmNmLTQ1OTctYjNmZC02NDNiMWE4MzkzMjkiLCJzdWIiOiIxNjY0NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0NCwiZXhwIjoxNjA3NjQ1NzQ0fQ.AYnyLL-ZzH_jSF6nXdo8rBNylP5pW4C2x00QE0uhqG0
```

`POST /api/v1/company/denylisted_organizers/bulk`

#### Parameters


```json
{"data":{"type":"attendee","attributes":{"email_list":"test@test.com,test2@test.com"}}}
```


| Name | Description |
|:-----|:------------|
| email_list *required* |  email list |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": [
    {
      "id": "510",
      "type": "denylisted_organizers",
      "attributes": {
        "email": "test@test.com",
        "owner_type": "Team",
        "owner_id": 17237
      }
    },
    {
      "id": "511",
      "type": "denylisted_organizers",
      "attributes": {
        "email": "test2@test.com",
        "owner_type": "Team",
        "owner_id": 17237
      }
    }
  ]
}
```



```shell
curl "http://localhost:3000/api/v1/company/denylisted_organizers/bulk" -d '{"data":{"type":"attendee","attributes":{"email_list":"test@test.com,test2@test.com"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NDNmMWJlOC0wMmNmLTQ1OTctYjNmZC02NDNiMWE4MzkzMjkiLCJzdWIiOiIxNjY0NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0NCwiZXhwIjoxNjA3NjQ1NzQ0fQ.AYnyLL-ZzH_jSF6nXdo8rBNylP5pW4C2x00QE0uhqG0"
```
## Bulk create deny-list entries for user


### Request

#### Endpoint

```plaintext
POST /api/v1/users/denylisted_organizers/bulk
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxNzYzMzc5Ni04ODU2LTQ0NGMtOTA4Yy0wMmZhMWI1YWNlZmMiLCJzdWIiOiIxNjY0NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0NCwiZXhwIjoxNjA3NjQ1NzQ0fQ.60y6bZHE9HEiXy7swYSo2djJk2GpbrCWtbh71_pY4oE
```

`POST /api/v1/users/denylisted_organizers/bulk`

#### Parameters


```json
{"data":{"type":"attendee","attributes":{"email_list":"test@test.com,test2@test.com"}}}
```


| Name | Description |
|:-----|:------------|
| email_list *required* |  email list |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": [
    {
      "id": "508",
      "type": "denylisted_organizers",
      "attributes": {
        "email": "test@test.com",
        "owner_type": "User",
        "owner_id": 16645
      }
    },
    {
      "id": "509",
      "type": "denylisted_organizers",
      "attributes": {
        "email": "test2@test.com",
        "owner_type": "User",
        "owner_id": 16645
      }
    }
  ]
}
```



```shell
curl "http://localhost:3000/api/v1/users/denylisted_organizers/bulk" -d '{"data":{"type":"attendee","attributes":{"email_list":"test@test.com,test2@test.com"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxNzYzMzc5Ni04ODU2LTQ0NGMtOTA4Yy0wMmZhMWI1YWNlZmMiLCJzdWIiOiIxNjY0NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0NCwiZXhwIjoxNjA3NjQ1NzQ0fQ.60y6bZHE9HEiXy7swYSo2djJk2GpbrCWtbh71_pY4oE"
```
## Create deny-list entry for company


### Request

#### Endpoint

```plaintext
POST /api/v1/company/denylisted_organizers
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4OTViMGY0Ny1lMDEyLTQ0MzMtYjQ1MC1lNjIzYjM2OTZjYTMiLCJzdWIiOiIxNjY0NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0NCwiZXhwIjoxNjA3NjQ1NzQ0fQ.dIfg6w9WI4j889se2sH00Bth6gCIb6mjKzPGRgDTkAs
```

`POST /api/v1/company/denylisted_organizers`

#### Parameters


```json
{"data":{"type":"attendee","attributes":{"email":"test@test.com"}}}
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "512",
    "type": "denylisted_organizers",
    "attributes": {
      "email": "test@test.com",
      "owner_type": "Team",
      "owner_id": 17238
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/company/denylisted_organizers" -d '{"data":{"type":"attendee","attributes":{"email":"test@test.com"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4OTViMGY0Ny1lMDEyLTQ0MzMtYjQ1MC1lNjIzYjM2OTZjYTMiLCJzdWIiOiIxNjY0NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0NCwiZXhwIjoxNjA3NjQ1NzQ0fQ.dIfg6w9WI4j889se2sH00Bth6gCIb6mjKzPGRgDTkAs"
```
## Create deny-list entry for user


### Request

#### Endpoint

```plaintext
POST /api/v1/users/denylisted_organizers
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiZGIxOTVhNy01YWQ4LTRkMDAtODBmMC02YzdhOGE5Mjc0YjMiLCJzdWIiOiIxNjY0MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MywiZXhwIjoxNjA3NjQ1NzQzfQ.xu8IUXl7BLEg16LR6bZ8_fz5DUnDxorIw9uThZal-CI
```

`POST /api/v1/users/denylisted_organizers`

#### Parameters


```json
{"data":{"type":"attendee","attributes":{"email":"test@test.com"}}}
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "506",
    "type": "denylisted_organizers",
    "attributes": {
      "email": "test@test.com",
      "owner_type": "User",
      "owner_id": 16643
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/users/denylisted_organizers" -d '{"data":{"type":"attendee","attributes":{"email":"test@test.com"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiZGIxOTVhNy01YWQ4LTRkMDAtODBmMC02YzdhOGE5Mjc0YjMiLCJzdWIiOiIxNjY0MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MywiZXhwIjoxNjA3NjQ1NzQzfQ.xu8IUXl7BLEg16LR6bZ8_fz5DUnDxorIw9uThZal-CI"
```
## List denied organizers for company


### Request

#### Endpoint

```plaintext
GET /api/v1/company/denylisted_organizers
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0Yjg0OGQ5MC1jYmFkLTQ0NDQtYTYxYS1hNWRlYTY4ODBmYjgiLCJzdWIiOiIxNjY0OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0NCwiZXhwIjoxNjA3NjQ1NzQ0fQ.ElWE9DKJrK7aGhchtjOvNvOlN2zCpKNx_RavYLvX70M
```

`GET /api/v1/company/denylisted_organizers`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "514",
      "type": "denylisted_organizers",
      "attributes": {
        "email": "test44@test.com",
        "owner_type": "Team",
        "owner_id": 17240
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/company/denylisted_organizers" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0Yjg0OGQ5MC1jYmFkLTQ0NDQtYTYxYS1hNWRlYTY4ODBmYjgiLCJzdWIiOiIxNjY0OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0NCwiZXhwIjoxNjA3NjQ1NzQ0fQ.ElWE9DKJrK7aGhchtjOvNvOlN2zCpKNx_RavYLvX70M"
```
## List denied organizers for user


### Request

#### Endpoint

```plaintext
GET /api/v1/users/denylisted_organizers
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNjg3MjcyNS05Mjg3LTQ1YTctYjE3ZC04OGE3YzMyOTNjN2EiLCJzdWIiOiIxNjY0NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0NCwiZXhwIjoxNjA3NjQ1NzQ0fQ.CDqx10JMpalQfCB7e0Ub3ThMtooZaSpqCWWvANjlNU4
```

`GET /api/v1/users/denylisted_organizers`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "507",
      "type": "denylisted_organizers",
      "attributes": {
        "email": "test44@test.com",
        "owner_type": "User",
        "owner_id": 16644
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/users/denylisted_organizers" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNjg3MjcyNS05Mjg3LTQ1YTctYjE3ZC04OGE3YzMyOTNjN2EiLCJzdWIiOiIxNjY0NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0NCwiZXhwIjoxNjA3NjQ1NzQ0fQ.CDqx10JMpalQfCB7e0Ub3ThMtooZaSpqCWWvANjlNU4"
```
## Remove denied organizer for company


### Request

#### Endpoint

```plaintext
DELETE /api/v1/company/denylisted_organizers/513
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhNTU5ZDAwNC02MzgzLTQxNjEtOTdlNi02YzM4NDY5OWI2ZGYiLCJzdWIiOiIxNjY0OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0NCwiZXhwIjoxNjA3NjQ1NzQ0fQ.3Y2C7lhNU2HjdBkqehUBGnnfUrwDNwSAGAFAa2Lwfwk
```

`DELETE /api/v1/company/denylisted_organizers/:id`

#### Parameters


None known.


### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/company/denylisted_organizers/513" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhNTU5ZDAwNC02MzgzLTQxNjEtOTdlNi02YzM4NDY5OWI2ZGYiLCJzdWIiOiIxNjY0OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0NCwiZXhwIjoxNjA3NjQ1NzQ0fQ.3Y2C7lhNU2HjdBkqehUBGnnfUrwDNwSAGAFAa2Lwfwk"
```
## Remove denied organizer for user


### Request

#### Endpoint

```plaintext
DELETE /api/v1/users/denylisted_organizers/505
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmYTA5NWZlMS1jNjIzLTQ0ZDItYjY0MS0wZDUyZDhkMTMzYmQiLCJzdWIiOiIxNjY0MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MywiZXhwIjoxNjA3NjQ1NzQzfQ.c0HYS-iiyKDPCmNyUdVcBBdLtWpqg4o2OmkpVit9hZA
```

`DELETE /api/v1/users/denylisted_organizers/:id`

#### Parameters


None known.


### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/users/denylisted_organizers/505" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmYTA5NWZlMS1jNjIzLTQ0ZDItYjY0MS0wZDUyZDhkMTMzYmQiLCJzdWIiOiIxNjY0MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTc0MywiZXhwIjoxNjA3NjQ1NzQzfQ.c0HYS-iiyKDPCmNyUdVcBBdLtWpqg4o2OmkpVit9hZA"
```
# Ping



## Authenticated Ping


### Request

#### Endpoint

```plaintext
GET /api/v1/ping
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0NGEzMjkwMS02ZTQ2LTQzNWEtOTdlYy01NmNkOWNjYzVmMDkiLCJzdWIiOiIxNjU1MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOSwiZXhwIjoxNjA3NjQ1NzI5fQ.Cy3IL6ookVp2LOWrzyVmnIpukrZCD0h5npauyJj4UwA
```

`GET /api/v1/ping`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "f83369f3-39bc-4e61-b1be-d74f9ce7c127",
    "type": "pings",
    "attributes": {
      "id": "f83369f3-39bc-4e61-b1be-d74f9ce7c127",
      "date": "2020-11-16T00:15:29.970Z"
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/ping" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0NGEzMjkwMS02ZTQ2LTQzNWEtOTdlYy01NmNkOWNjYzVmMDkiLCJzdWIiOiIxNjU1MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOSwiZXhwIjoxNjA3NjQ1NzI5fQ.Cy3IL6ookVp2LOWrzyVmnIpukrZCD0h5npauyJj4UwA"
```
# Pre-Work Items



## Create prework item


### Request

#### Endpoint

```plaintext
POST /api/v1/meetings/7761/prework_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlZDkyZDhlYy1iYzhlLTRmNGEtODA3ZS1lNGRlNGNiZDZmNGUiLCJzdWIiOiIxNjYxNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOSwiZXhwIjoxNjA3NjQ1NzM5fQ.EF1CLIoTYEgyrQzYWMzyyl3Gc6ac4VeKAXxgTFbOZOQ
```

`POST /api/v1/meetings/:meeting_id/prework_items`

#### Parameters


```json
{"data":{"type":"prework_item","attributes":{"description":"Review the sales report","url":"https://www.locationtofile.com/salesreport.xls","timebox":3600}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| timebox  | Max amount of time that should be spent in seconds |
| url  |  url |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "618",
    "type": "prework_items",
    "attributes": {
      "id": 618,
      "description": "Review the sales report",
      "url": "https://www.locationtofile.com/salesreport.xls",
      "timebox": 3600
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/7761/prework_items" -d '{"data":{"type":"prework_item","attributes":{"description":"Review the sales report","url":"https://www.locationtofile.com/salesreport.xls","timebox":3600}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlZDkyZDhlYy1iYzhlLTRmNGEtODA3ZS1lNGRlNGNiZDZmNGUiLCJzdWIiOiIxNjYxNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOSwiZXhwIjoxNjA3NjQ1NzM5fQ.EF1CLIoTYEgyrQzYWMzyyl3Gc6ac4VeKAXxgTFbOZOQ"
```
## Delete prework item


### Request

#### Endpoint

```plaintext
DELETE /api/v1/meetings/7759/prework_items/616
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwODQ5ZDk2MC02MGI1LTQ1ODgtOTFiNC05MjRlMThiMTk0YmIiLCJzdWIiOiIxNjYxNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOSwiZXhwIjoxNjA3NjQ1NzM5fQ.gXbCyT9jaUbwBsG7Dzv0ZUy0Lku2iII6pq4T5tjgV8A
```

`DELETE /api/v1/meetings/:meeting_id/prework_items/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| timebox  | Max amount of time that should be spent in seconds |
| url  |  url |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/meetings/7759/prework_items/616" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwODQ5ZDk2MC02MGI1LTQ1ODgtOTFiNC05MjRlMThiMTk0YmIiLCJzdWIiOiIxNjYxNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOSwiZXhwIjoxNjA3NjQ1NzM5fQ.gXbCyT9jaUbwBsG7Dzv0ZUy0Lku2iII6pq4T5tjgV8A"
```
## List prework items


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7762/prework_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4ZDY0NmZjMy01ZjI3LTQ4MWYtOTgyZi1jZTBiZGFkOTFlNWIiLCJzdWIiOiIxNjYxOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOSwiZXhwIjoxNjA3NjQ1NzM5fQ.HIAKOZe4PThPR5BroMG-VGSEQbQgyT9Zh9uiRFBfQ6I
```

`GET /api/v1/meetings/:meeting_id/prework_items`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| timebox  | Max amount of time that should be spent in seconds |
| url  |  url |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "619",
      "type": "prework_items",
      "attributes": {
        "id": 619,
        "description": "Organic kombucha humblebrag cold-pressed 8-bit chillwave.",
        "url": "http://oberbrunner.co/karl_runolfsson",
        "timebox": 3600
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7762/prework_items" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4ZDY0NmZjMy01ZjI3LTQ4MWYtOTgyZi1jZTBiZGFkOTFlNWIiLCJzdWIiOiIxNjYxOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOSwiZXhwIjoxNjA3NjQ1NzM5fQ.HIAKOZe4PThPR5BroMG-VGSEQbQgyT9Zh9uiRFBfQ6I"
```
## Show prework item


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/7758/prework_items/615
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyN2M3ZmI4OC02MTVmLTQ0YzctYjg1Yi02Mzc3Yzg2YTFlNzgiLCJzdWIiOiIxNjYxNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOSwiZXhwIjoxNjA3NjQ1NzM5fQ.dJleHvimEidPzPvqvOb8lE7aSmuZ4NDzAt3Gt0JEQ9M
```

`GET /api/v1/meetings/:meeting_id/prework_items/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| timebox  | Max amount of time that should be spent in seconds |
| url  |  url |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "615",
    "type": "prework_items",
    "attributes": {
      "id": 615,
      "description": "Hella celiac schlitz franzen gentrify you probably haven't heard of them wayfarers gluten-free.",
      "url": "http://luettgen-donnelly.net/mimi.ullrich",
      "timebox": 3600
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/7758/prework_items/615" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyN2M3ZmI4OC02MTVmLTQ0YzctYjg1Yi02Mzc3Yzg2YTFlNzgiLCJzdWIiOiIxNjYxNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOSwiZXhwIjoxNjA3NjQ1NzM5fQ.dJleHvimEidPzPvqvOb8lE7aSmuZ4NDzAt3Gt0JEQ9M"
```
## Update prework item


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/7760/prework_items/617
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxMTYzZjFmMS1iOGIzLTRhYmMtYTdmMC1mOWE4ZjZkMzRkZTUiLCJzdWIiOiIxNjYxNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOSwiZXhwIjoxNjA3NjQ1NzM5fQ.vbeA9BJjyM71hQXiseAaaLSD81kIjQUrwjgMb36ShTg
```

`PUT /api/v1/meetings/:meeting_id/prework_items/:id`

#### Parameters


```json
{"data":{"type":"prework_item","attributes":{"description":"Review the sales report dude"}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| timebox  | Max amount of time that should be spent in seconds |
| url  |  url |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "617",
    "type": "prework_items",
    "attributes": {
      "id": 617,
      "description": "Review the sales report dude",
      "url": "http://hintz.info/shayna",
      "timebox": 3600
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/7760/prework_items/617" -d '{"data":{"type":"prework_item","attributes":{"description":"Review the sales report dude"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxMTYzZjFmMS1iOGIzLTRhYmMtYTdmMC1mOWE4ZjZkMzRkZTUiLCJzdWIiOiIxNjYxNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOSwiZXhwIjoxNjA3NjQ1NzM5fQ.vbeA9BJjyM71hQXiseAaaLSD81kIjQUrwjgMb36ShTg"
```
# Reporting

Meeting Evaluation Reporting

## Average Number of Attendees


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/average_attendees?by_period[starts_at]=2020-11-16+00%3A15%3A31+UTC&amp;by_period[ends_at]=2020-11-23+00%3A15%3A31+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmNDljNDkxNS1jNmFiLTRiMzEtYjZmNC1hZDkxN2FjODM1MDAiLCJzdWIiOiIxNjU2MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMSwiZXhwIjoxNjA3NjQ1NzMxfQ.qk3DmOt5hkHzTk6By2fRgEXI1qAMgpaEz_oRNIGg9JY
```

`GET /api/v1/reporting/user/evaluations/average_attendees`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-11-16 00:15:31 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-23 00:15:31 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "5538f2df-0ccc-40cb-b21a-ec9a07e175f2",
    "type": "reports",
    "attributes": {
      "name": "Attendees",
      "starts_at": "2020-11-16T00:00:00.000Z",
      "ends_at": "2020-11-23T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
      },
      "trends": null,
      "average": null,
      "total": 0.0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/average_attendees?by_period[starts_at]=2020-11-16+00%3A15%3A31+UTC&by_period[ends_at]=2020-11-23+00%3A15%3A31+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmNDljNDkxNS1jNmFiLTRiMzEtYjZmNC1hZDkxN2FjODM1MDAiLCJzdWIiOiIxNjU2MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMSwiZXhwIjoxNjA3NjQ1NzMxfQ.qk3DmOt5hkHzTk6By2fRgEXI1qAMgpaEz_oRNIGg9JY"
```
## Average scores per evaluator


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/averages?by_period[starts_at]=2020-11-16+00%3A15%3A30+UTC&amp;by_period[ends_at]=2020-11-23+00%3A15%3A30+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNzRhMjRlMS05YTU5LTQ1MDUtODBjZS02YmFiMTI2NDMyZGUiLCJzdWIiOiIxNjU1OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMCwiZXhwIjoxNjA3NjQ1NzMwfQ.haLcPmaw3zZ99sac-Zv29boaPeNdTazwlntyOnV5IRI
```

`GET /api/v1/reporting/user/evaluations/averages`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-11-16 00:15:30 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-23 00:15:30 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "3665b902-0116-4b37-a55f-5a49926a9b7e",
    "type": "reports",
    "attributes": {
      "name": "Evaluation averages and totals",
      "starts_at": "2020-11-16T00:00:00.000Z",
      "ends_at": "2020-11-23T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
        "totals": {
          "compliant": 0.0,
          "non_compliant": 0.0,
          "duration": 0.0
        },
        "counts": {
          "good": {
          },
          "bad": {
          }
        },
        "quality_label": "What would make these meetings more effective?"
      },
      "trends": null,
      "average": 0.0,
      "total": 0.0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/averages?by_period[starts_at]=2020-11-16+00%3A15%3A30+UTC&by_period[ends_at]=2020-11-23+00%3A15%3A30+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNzRhMjRlMS05YTU5LTQ1MDUtODBjZS02YmFiMTI2NDMyZGUiLCJzdWIiOiIxNjU1OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMCwiZXhwIjoxNjA3NjQ1NzMwfQ.haLcPmaw3zZ99sac-Zv29boaPeNdTazwlntyOnV5IRI"
```
## Company User Counts


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/team/evaluations/user_counts?by_period[starts_at]=2020-11-16+00%3A15%3A33+UTC&amp;by_period[ends_at]=2020-11-23+00%3A15%3A33+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxMzI0NTU4ZC02YzljLTQ0OGQtYjQxOS1kM2VjM2FiYTYzZDIiLCJzdWIiOiIxNjU4MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNCwiZXhwIjoxNjA3NjQ1NzM0fQ.1dBH5RyU32JA1sY1M7kwbR-lIDJMcHq8ztdF30mP47M
```

`GET /api/v1/reporting/team/evaluations/user_counts`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-11-16 00:15:33 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-23 00:15:33 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "9397b572-539c-47c7-8c80-2951472e5c1f",
    "type": "reports",
    "attributes": {
      "name": "Team User Count",
      "starts_at": "2020-11-16T00:00:00.000Z",
      "ends_at": "2020-11-23T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
        "evaluatable_users": 0,
        "total_users": 1
      },
      "trends": null,
      "average": 0,
      "total": 0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/team/evaluations/user_counts?by_period[starts_at]=2020-11-16+00%3A15%3A33+UTC&by_period[ends_at]=2020-11-23+00%3A15%3A33+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxMzI0NTU4ZC02YzljLTQ0OGQtYjQxOS1kM2VjM2FiYTYzZDIiLCJzdWIiOiIxNjU4MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNCwiZXhwIjoxNjA3NjQ1NzM0fQ.1dBH5RyU32JA1sY1M7kwbR-lIDJMcHq8ztdF30mP47M"
```
## Duration and Cost Details


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/duration_and_cost_details?by_period[starts_at]=2020-11-16+00%3A15%3A31+UTC&amp;by_period[ends_at]=2020-11-23+00%3A15%3A31+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyNGUwNmMxNi1lYzA1LTRlYWMtOWY0YS1mNGMxMzIxYjk3MjQiLCJzdWIiOiIxNjU2MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMSwiZXhwIjoxNjA3NjQ1NzMxfQ.4IFf4vMemux8zGLekED0wAhz0IOUR0v0ceKxMdFm0VU
```

`GET /api/v1/reporting/user/evaluations/duration_and_cost_details`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-11-16 00:15:31 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-23 00:15:31 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "07e5ce64-ad29-4696-bfc7-7798ccadc5a9",
    "type": "reports",
    "attributes": {
      "name": "Duration and Costs Details",
      "starts_at": "2020-11-16T00:00:00.000Z",
      "ends_at": "2020-11-23T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
        "categories": {
        },
        "intentions": {
        }
      },
      "trends": null,
      "average": 0,
      "total": 0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/duration_and_cost_details?by_period[starts_at]=2020-11-16+00%3A15%3A31+UTC&by_period[ends_at]=2020-11-23+00%3A15%3A31+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyNGUwNmMxNi1lYzA1LTRlYWMtOWY0YS1mNGMxMzIxYjk3MjQiLCJzdWIiOiIxNjU2MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMSwiZXhwIjoxNjA3NjQ1NzMxfQ.4IFf4vMemux8zGLekED0wAhz0IOUR0v0ceKxMdFm0VU"
```
## Duration and Costs


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/duration_and_costs?by_period[starts_at]=2020-11-16+00%3A15%3A30+UTC&amp;by_period[ends_at]=2020-11-23+00%3A15%3A30+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0MjdiMDZiYS03ZjVmLTQwM2MtOTA4ZC01ZDM2M2Q3ZDAzYWIiLCJzdWIiOiIxNjU1NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMCwiZXhwIjoxNjA3NjQ1NzMwfQ.EX2rGioigpaFnqIPc67aNpJ1EggNtWudWSQ6SVG9zfE
```

`GET /api/v1/reporting/user/evaluations/duration_and_costs`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-11-16 00:15:30 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-23 00:15:30 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "5046b2db-bce4-428b-a513-6d37d99c944f",
    "type": "reports",
    "attributes": {
      "name": "Duration and Costs Summary",
      "starts_at": "2020-11-16T00:00:00.000Z",
      "ends_at": "2020-11-23T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
        "annual_salary": 75000,
        "estimated_hourly_pay": 38,
        "good": {
          "meetings": 0,
          "meeting_duration": 0,
          "attendee_total": 0,
          "ave_attendee_per_meeting": 0.0,
          "meeting_cost_total": 0.0,
          "meeting_cost_per_hour": null,
          "ave_cost_per_meeting": null
        },
        "bad": {
          "meetings": 0,
          "meeting_duration": 0,
          "attendee_total": 0,
          "ave_attendee_per_meeting": 0.0,
          "meeting_cost_total": 0.0,
          "meeting_cost_per_hour": null,
          "ave_cost_per_meeting": null
        },
        "total": {
          "meetings": 0,
          "meeting_duration": 0,
          "ave_meeting_duration": 0,
          "attendee_total": 0,
          "ave_attendee_per_meeting": 0.0,
          "meeting_cost_total": 0.0,
          "meeting_cost_per_hour": null,
          "ave_cost_per_meeting": null,
          "work_hours": 48.0,
          "work_hours_spent": {
            "spent_hours": 0.0,
            "percent_of_time": 0.0
          }
        }
      },
      "trends": null,
      "average": null,
      "total": 0.0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/duration_and_costs?by_period[starts_at]=2020-11-16+00%3A15%3A30+UTC&by_period[ends_at]=2020-11-23+00%3A15%3A30+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0MjdiMDZiYS03ZjVmLTQwM2MtOTA4ZC01ZDM2M2Q3ZDAzYWIiLCJzdWIiOiIxNjU1NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMCwiZXhwIjoxNjA3NjQ1NzMwfQ.EX2rGioigpaFnqIPc67aNpJ1EggNtWudWSQ6SVG9zfE"
```
## Late Scheduled Meetings


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/scheduled_late?by_period[starts_at]=2020-11-16+00%3A15%3A31+UTC&amp;by_period[ends_at]=2020-11-23+00%3A15%3A31+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyMGY3ZDY4Yy1lMzk0LTQwZGYtOTJkYi05MTY2MzI0YTA2ZTgiLCJzdWIiOiIxNjU2MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMSwiZXhwIjoxNjA3NjQ1NzMxfQ.H1DrEKp1OTY01aPi1rHY-yL7EBGAJ3ZvxYd45TsYegs
```

`GET /api/v1/reporting/user/evaluations/scheduled_late`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-11-16 00:15:31 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-23 00:15:31 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "6feb4180-aa0f-4ce2-93ce-12d936894b75",
    "type": "reports",
    "attributes": {
      "name": "Scheduled late",
      "starts_at": "2020-11-16T00:00:00.000Z",
      "ends_at": "2020-11-23T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
      },
      "trends": null,
      "average": 0.0,
      "total": 0.0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/scheduled_late?by_period[starts_at]=2020-11-16+00%3A15%3A31+UTC&by_period[ends_at]=2020-11-23+00%3A15%3A31+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyMGY3ZDY4Yy1lMzk0LTQwZGYtOTJkYi05MTY2MzI0YTA2ZTgiLCJzdWIiOiIxNjU2MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMSwiZXhwIjoxNjA3NjQ1NzMxfQ.H1DrEKp1OTY01aPi1rHY-yL7EBGAJ3ZvxYd45TsYegs"
```
## Overtime Meeting Hours


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/overtime?by_period[starts_at]=2020-11-16+00%3A15%3A31+UTC&amp;by_period[ends_at]=2020-11-23+00%3A15%3A31+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5MThiNDkxNC02ZDIzLTRjOGMtYjQ0MC05OGYxMDdlNzU1NDMiLCJzdWIiOiIxNjU2MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMSwiZXhwIjoxNjA3NjQ1NzMxfQ.ePTg_OkY4fn8BgCEuRfp0C3mgdtFNQbVJUNYJRkU7LI
```

`GET /api/v1/reporting/user/evaluations/overtime`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-11-16 00:15:31 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-23 00:15:31 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "13acedf3-a0f5-41fe-b922-dff01156f340",
    "type": "reports",
    "attributes": {
      "name": "Overtime",
      "starts_at": "2020-11-16T00:00:00.000Z",
      "ends_at": "2020-11-23T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
      },
      "trends": null,
      "average": 0,
      "total": 0.0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/overtime?by_period[starts_at]=2020-11-16+00%3A15%3A31+UTC&by_period[ends_at]=2020-11-23+00%3A15%3A31+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5MThiNDkxNC02ZDIzLTRjOGMtYjQ0MC05OGYxMDdlNzU1NDMiLCJzdWIiOiIxNjU2MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMSwiZXhwIjoxNjA3NjQ1NzMxfQ.ePTg_OkY4fn8BgCEuRfp0C3mgdtFNQbVJUNYJRkU7LI"
```
## Wellness Block Conflicts


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/focus_block_conflict?by_period[starts_at]=2020-11-16+00%3A15%3A30+UTC&amp;by_period[ends_at]=2020-11-23+00%3A15%3A30+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwZDFlNmE1Ni00NjQ1LTQ2ZWQtOTIxNi05ZThjZWZiOTMyNmMiLCJzdWIiOiIxNjU1OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMSwiZXhwIjoxNjA3NjQ1NzMxfQ.qbIDwMwlqcBcB048kaD2YNvC-9-HZUAnm0dz1KdYwRw
```

`GET /api/v1/reporting/user/evaluations/focus_block_conflict`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-11-16 00:15:30 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-23 00:15:30 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "47639b86-c9b9-442e-87ff-13d046dfc250",
    "type": "reports",
    "attributes": {
      "name": "Focus block conflict",
      "starts_at": "2020-11-16T00:00:00.000Z",
      "ends_at": "2020-11-23T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
      },
      "trends": null,
      "average": 0.0,
      "total": 0.0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/focus_block_conflict?by_period[starts_at]=2020-11-16+00%3A15%3A30+UTC&by_period[ends_at]=2020-11-23+00%3A15%3A30+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwZDFlNmE1Ni00NjQ1LTQ2ZWQtOTIxNi05ZThjZWZiOTMyNmMiLCJzdWIiOiIxNjU1OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMSwiZXhwIjoxNjA3NjQ1NzMxfQ.qbIDwMwlqcBcB048kaD2YNvC-9-HZUAnm0dz1KdYwRw"
```
# Settings Labels



## List settings labels


### Request

#### Endpoint

```plaintext
GET /api/v1/settings_labels
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNTAyMzE3MC0yMTJkLTRjYTctODc4ZS1lMTBhY2U1YmRlMWQiLCJzdWIiOiIxNjU3MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMiwiZXhwIjoxNjA3NjQ1NzMyfQ.dTgVsCvVA0uQEfs1at3lM5ct3yQ7F3GQMHPE1tGWusI
```

`GET /api/v1/settings_labels`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "1dc8a681-cbf3-4836-946c-dd727ece9aa5",
    "type": "settings_labels",
    "attributes": {
      "list": {
        "focus_block_conflict": {
          "label": "Wellness block conflict",
          "negative_label": "Wellness block conflicts",
          "positive_label": "No wellness block conflicts",
          "description": "Virtually sacred time set aside for getting work done.",
          "weight": 0.21
        },
        "meeting_conflict": {
          "label": "Meeting conflict",
          "negative_label": "Meeting conflicts",
          "positive_label": "No meeting conflicts",
          "description": "Meeting scheduled over one already accepted -- or one that the invitee created themselves.",
          "weight": 0.16
        },
        "last_minute_schedule": {
          "label": "Last minute invite",
          "negative_label": "Scheduled last minute",
          "positive_label": "Scheduled on-time",
          "description": "Hours ahead of time that a meeting must be scheduled.",
          "weight": 0.16
        },
        "compliance_deadline": {
          "label": "Deadline",
          "description": "Hours ahead of a meeting before it's considered 'not compliant'."
        },
        "non_compliance_action": {
          "label": "Action to take",
          "description": "Action when meeting requirements are not met before deadline.",
          "premium": true
        },
        "max_attendees": {
          "label": "Number of attendees",
          "negative_label": "Too many people",
          "positive_label": "Good amount of people",
          "description": "Max # of people in a meeting. Ignored for \"all hands\" and all-day meetings.",
          "weight": 0.06
        },
        "desired_duration": {
          "label": "Ideal meeting duration",
          "negative_label": "Meeting is too long",
          "positive_label": "Good meeting duration",
          "description": "Meeting length goal.",
          "weight": 0.06
        },
        "required_agenda": {
          "label": "Agenda",
          "negative_label": "Missing an agenda",
          "positive_label": "Has an agenda",
          "description": "Time-boxed items to discuss.",
          "weight": 0.21
        },
        "required_category": {
          "label": "Category",
          "negative_label": "Missing a category",
          "positive_label": "Has a category",
          "description": "Type of meeting being created.",
          "weight": null
        },
        "required_intention": {
          "label": "Intention",
          "negative_label": "Missing an intention",
          "positive_label": "Has an intention",
          "description": "The reason for meeting.",
          "weight": 0.06
        },
        "required_objectives": {
          "label": "Objectives",
          "negative_label": "Missing objective(s)",
          "positive_label": "Has objective(s)",
          "description": "Goals of the meeting.",
          "weight": 0.11
        },
        "required_prework": {
          "label": "Pre-work",
          "negative_label": "Pre-work is needed",
          "positive_label": "Pre-work is done",
          "description": "Tasks and/or associated materials to address beforehand.",
          "weight": null
        },
        "required_outcomes": {
          "label": "Outcomes",
          "negative_label": "Missing outcomes",
          "positive_label": "Has outcomes",
          "description": "Post-meeting notes with next steps.",
          "weight": null,
          "coming_soon": true
        },
        "required_role_leader": {
          "label": "Assigned leader",
          "negative_label": "Missing an assigned leader",
          "positive_label": "A leader is assigned",
          "description": "To lead the meeting.",
          "weight": null,
          "coming_soon": true
        },
        "required_role_time_keeper": {
          "label": "Assigned Time-keeper",
          "negative_label": "Missing an assigned time-keeper",
          "positive_label": "A time-keeper is assigned",
          "description": "To keep it on track.",
          "weight": null,
          "coming_soon": true
        },
        "required_role_recorder": {
          "label": "Assigned Note-taker",
          "negative_label": "Missing an assigned note-taker",
          "positive_label": "A note-taker is assigned",
          "description": "To capture parking lot items and outcomes.",
          "weight": null,
          "coming_soon": true
        },
        "required_attendee_roles": {
          "label": "Assign all roles",
          "negative_label": "Missing assigned meeting roles",
          "positive_label": "Meeting roles are assigned",
          "description": "All of the attendee roles are need to be assigned.",
          "weight": null,
          "coming_soon": true
        },
        "ignore_all_day_meetings": {
          "label": "All-day meetings",
          "description": "Do not evaluate all day meetings."
        },
        "ignore_all_hands_meetings": {
          "label": "All-hands meetings",
          "description": "Do not evaluate all hands meetings."
        }
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/settings_labels" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNTAyMzE3MC0yMTJkLTRjYTctODc4ZS1lMTBhY2U1YmRlMWQiLCJzdWIiOiIxNjU3MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMiwiZXhwIjoxNjA3NjQ1NzMyfQ.dTgVsCvVA0uQEfs1at3lM5ct3yQ7F3GQMHPE1tGWusI"
```
# Stripe

Stripe Subscriptions

## Create Stripe Session


### Request

#### Endpoint

```plaintext
POST /api/v1/stripe_checkout/sessions
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2Yzg1MjI0MC01ZTFlLTQ5N2ItODkzNy1mNTgwYjFjNzBiNTEiLCJzdWIiOiIxNjU3NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMywiZXhwIjoxNjA3NjQ1NzMzfQ.arA5VaaLKLNQH8Te_gQkaULnMSf9SQSbxkn0fwRU-Ig
```

`POST /api/v1/stripe_checkout/sessions`

#### Parameters


```json
{"data":{"type":"stripe_sessions","attributes":{"key":"team-400"}}}
```

None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "test_cs_1",
    "type": "stripe_sessions",
    "attributes": {
      "item": {
        "plan": "team-400",
        "quantity": 1
      },
      "status": "in_progress"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/stripe_checkout/sessions" -d '{"data":{"type":"stripe_sessions","attributes":{"key":"team-400"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2Yzg1MjI0MC01ZTFlLTQ5N2ItODkzNy1mNTgwYjFjNzBiNTEiLCJzdWIiOiIxNjU3NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMywiZXhwIjoxNjA3NjQ1NzMzfQ.arA5VaaLKLNQH8Te_gQkaULnMSf9SQSbxkn0fwRU-Ig"
```
## Delete Stripe Subscription


### Request

#### Endpoint

```plaintext
DELETE /api/v1/subscription
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3OGZlN2VkYS01ZmI4LTQxMDItYmRkMC03NzMwODRmZDIwOGYiLCJzdWIiOiIxNjUwMSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMiwiZXhwIjoxNjA3NjQ1NzIyfQ.dZ6fFqz89NKbexxALgtwAHQ_F1fWKjhpRh7yR_zMRfY
```

`DELETE /api/v1/subscription`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "815",
    "type": "subscriptions",
    "attributes": {
      "stripe_id": "test_su_4",
      "active": false,
      "created_at": "2020-11-16T00:15:22.293Z",
      "current_period_start": "2020-11-16T00:15:22.000Z",
      "current_period_end": "2020-12-16T00:15:22.000Z",
      "amount": 151,
      "category": "team",
      "plan": "pro",
      "product_id": "team"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/subscription" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3OGZlN2VkYS01ZmI4LTQxMDItYmRkMC03NzMwODRmZDIwOGYiLCJzdWIiOiIxNjUwMSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMiwiZXhwIjoxNjA3NjQ1NzIyfQ.dZ6fFqz89NKbexxALgtwAHQ_F1fWKjhpRh7yR_zMRfY"
```
## Update Stripe Session


### Request

#### Endpoint

```plaintext
PUT /api/v1/stripe_checkout/sessions
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhMjYzNmY5Zi05NmEzLTQ1MGYtOWY0Ni0wYzhkODA3N2RkYzAiLCJzdWIiOiIxNjU3NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMywiZXhwIjoxNjA3NjQ1NzMzfQ.jppFw2GasOTxtRF6F0a0tCiQs7MLHtQgVR_7MI8f7VM
```

`PUT /api/v1/stripe_checkout/sessions`

#### Parameters


```json
{"data":{"type":"stripe_sessions","attributes":{"key":"team-400"}}}
```

None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "test_cs_1",
    "type": "stripe_sessions",
    "attributes": {
      "item": null,
      "status": "in_progress"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/stripe_checkout/sessions" -d '{"data":{"type":"stripe_sessions","attributes":{"key":"team-400"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhMjYzNmY5Zi05NmEzLTQ1MGYtOWY0Ni0wYzhkODA3N2RkYzAiLCJzdWIiOiIxNjU3NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMywiZXhwIjoxNjA3NjQ1NzMzfQ.jppFw2GasOTxtRF6F0a0tCiQs7MLHtQgVR_7MI8f7VM"
```
## Update Stripe Subscription


### Request

#### Endpoint

```plaintext
PUT /api/v1/subscription
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzYzk5ZTZjMS04NDBmLTQ0ODItYTA2Yy1hNjBmMmEwMDE4ZTkiLCJzdWIiOiIxNjUwMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMiwiZXhwIjoxNjA3NjQ1NzIyfQ.1Bawbt5gmVN62WvDtNAMaGItYslfNGZyYyxF2h-GIoE
```

`PUT /api/v1/subscription`

#### Parameters


```json
{"data":{"type":"subscriptions","attributes":{"key":"pro"}}}
```

None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "814",
    "type": "subscriptions",
    "attributes": {
      "stripe_id": "test_txn_default",
      "active": true,
      "created_at": "2020-11-16T00:15:22.108Z",
      "current_period_start": "2020-11-16T00:15:22.000Z",
      "current_period_end": "2020-12-16T00:15:22.000Z",
      "amount": 151,
      "category": "team",
      "plan": "pro",
      "product_id": "team"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/subscription" -d '{"data":{"type":"subscriptions","attributes":{"key":"pro"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzYzk5ZTZjMS04NDBmLTQ0ODItYTA2Yy1hNjBmMmEwMDE4ZTkiLCJzdWIiOiIxNjUwMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMiwiZXhwIjoxNjA3NjQ1NzIyfQ.1Bawbt5gmVN62WvDtNAMaGItYslfNGZyYyxF2h-GIoE"
```
# Subscription



## Show subscription


### Request

#### Endpoint

```plaintext
GET /api/v1/subscription
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyMDgyNzNmZC02MWQwLTRkMDgtOWFmMi1jMTVlM2E5ODBiY2IiLCJzdWIiOiIxNjU3OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMywiZXhwIjoxNjA3NjQ1NzMzfQ.FsooixngRwuG7x4021OcvGHjM3ROnj-TZGkwjAz4fuI
```

`GET /api/v1/subscription`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "822",
    "type": "subscriptions",
    "attributes": {
      "stripe_id": "tok_diners",
      "active": true,
      "created_at": "2020-11-16T00:15:33.708Z",
      "current_period_start": null,
      "current_period_end": null,
      "amount": 151,
      "category": "user",
      "plan": "team-151",
      "product_id": "team-400"
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/subscription" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyMDgyNzNmZC02MWQwLTRkMDgtOWFmMi1jMTVlM2E5ODBiY2IiLCJzdWIiOiIxNjU3OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMywiZXhwIjoxNjA3NjQ1NzMzfQ.FsooixngRwuG7x4021OcvGHjM3ROnj-TZGkwjAz4fuI"
```
# Subscription Plans



## List subscription plans


### Request

#### Endpoint

```plaintext
GET /api/v1/subscription_plans
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1MjQ4YjkzYS0xMmFlLTRlNDEtOTBhMS0yNjgzNWUwMTg0ZmEiLCJzdWIiOiIxNjU3MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMiwiZXhwIjoxNjA3NjQ1NzMyfQ.6ES-n4A7NCDKPOwh2mc4oQ0pyzBUnxzZpNyjv-rlVMs
```

`GET /api/v1/subscription_plans`

#### Parameters



| Name | Description |
|:-----|:------------|
| billing_admin *required* | User must be a billing admin |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [

  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/subscription_plans" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1MjQ4YjkzYS0xMmFlLTRlNDEtOTBhMS0yNjgzNWUwMTg0ZmEiLCJzdWIiOiIxNjU3MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczMiwiZXhwIjoxNjA3NjQ1NzMyfQ.6ES-n4A7NCDKPOwh2mc4oQ0pyzBUnxzZpNyjv-rlVMs"
```
# Team Invites



## Create invite


### Request

#### Endpoint

```plaintext
POST /api/v1/invites
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkNmVkOTRjMC0wMTcwLTRhYjQtYWI3Yy0yNTQzZWU5N2MwOTIiLCJzdWIiOiIxNjQ4NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcxOSwiZXhwIjoxNjA3NjQ1NzE5fQ.K4zfpLBFEx0F8j9s_R8YWUrk7f6HLobkjUx5LAqZihg
```

`POST /api/v1/invites`

#### Parameters


```json
{"data":{"type":"agenda_item","attributes":{"email":"ivan@little-bailey.com"}}}
```


| Name | Description |
|:-----|:------------|
| billing_admin *required* | User must be a billing admin |
| email *required* |  email |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "141",
    "type": "invites",
    "attributes": {
      "team_id": 17073,
      "user_id": 16485,
      "email": "ivan@little-bailey.com",
      "created_at": "2020-11-16T00:15:19.743Z",
      "accepted_at": "2020-11-16T00:15:19.800Z"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/invites" -d '{"data":{"type":"agenda_item","attributes":{"email":"ivan@little-bailey.com"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkNmVkOTRjMC0wMTcwLTRhYjQtYWI3Yy0yNTQzZWU5N2MwOTIiLCJzdWIiOiIxNjQ4NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcxOSwiZXhwIjoxNjA3NjQ1NzE5fQ.K4zfpLBFEx0F8j9s_R8YWUrk7f6HLobkjUx5LAqZihg"
```
## Delete invite


### Request

#### Endpoint

```plaintext
DELETE /api/v1/invites/140
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5ZTU5YTNhZS1lOTc2LTQ5YjUtODU4Ni0zM2U4YmM0MTZiZWQiLCJzdWIiOiIxNjQ4MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcxOSwiZXhwIjoxNjA3NjQ1NzE5fQ.KV8tx12u4XUQhrwEh9siXf-inkAZiviUKcG3ovIOwy8
```

`DELETE /api/v1/invites/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| billing_admin *required* | User must be a billing admin |
| email *required* |  email |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/invites/140" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5ZTU5YTNhZS1lOTc2LTQ5YjUtODU4Ni0zM2U4YmM0MTZiZWQiLCJzdWIiOiIxNjQ4MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcxOSwiZXhwIjoxNjA3NjQ1NzE5fQ.KV8tx12u4XUQhrwEh9siXf-inkAZiviUKcG3ovIOwy8"
```
## List invites


### Request

#### Endpoint

```plaintext
GET /api/v1/invites
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MTVlYmYzZS1iZWYyLTRjZDgtODA3Ni04NGZhM2Q4NmYwYjIiLCJzdWIiOiIxNjQ4NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMCwiZXhwIjoxNjA3NjQ1NzIwfQ.w6tlumCxTbhX5S7yGT4HY1Lx2IyZU8q559_UGv3aBdM
```

`GET /api/v1/invites`

#### Parameters



| Name | Description |
|:-----|:------------|
| billing_admin *required* | User must be a billing admin |
| email *required* |  email |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "142",
      "type": "invites",
      "attributes": {
        "team_id": 17076,
        "user_id": 16487,
        "email": "donald@emmerich.biz",
        "created_at": "2020-11-16T00:15:20.042Z",
        "accepted_at": null
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/invites" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MTVlYmYzZS1iZWYyLTRjZDgtODA3Ni04NGZhM2Q4NmYwYjIiLCJzdWIiOiIxNjQ4NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMCwiZXhwIjoxNjA3NjQ1NzIwfQ.w6tlumCxTbhX5S7yGT4HY1Lx2IyZU8q559_UGv3aBdM"
```
# Team Members



## Add membership to team


### Request

#### Endpoint

```plaintext
POST /api/v1/teams/17109/members
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5OGU5ZTQzMi03ZWM3LTRmZmYtYjBmMy0zMjA2MWI4YWE5MTkiLCJzdWIiOiIxNjUxOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNSwiZXhwIjoxNjA3NjQ1NzI1fQ.VIY0DKhphJjks0KFZGt41Ci-_GQvsKHelXpPiGGq8gk
```

`POST /api/v1/teams/:id/members`

#### Parameters


```json
{"data":{"type":"team","attributes":{"user_id":16521,"role":"billing_admin"}}}
```


| Name | Description |
|:-----|:------------|
| billing_admin *required* | User must be a billing admin |
| user_id *required* |  user |
| role  | user or billing_admin |
| licensed  | boolean |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "16784",
    "type": "memberships",
    "attributes": {
      "user_id": 16521,
      "role": "billing_admin",
      "name": "Beyonder Claw Monarch Eyes",
      "email": "test2@test.com",
      "licensed": false,
      "profile_image": "http://goyette.co/marisa"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/teams/17109/members" -d '{"data":{"type":"team","attributes":{"user_id":16521,"role":"billing_admin"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5OGU5ZTQzMi03ZWM3LTRmZmYtYjBmMy0zMjA2MWI4YWE5MTkiLCJzdWIiOiIxNjUxOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNSwiZXhwIjoxNjA3NjQ1NzI1fQ.VIY0DKhphJjks0KFZGt41Ci-_GQvsKHelXpPiGGq8gk"
```
## Delete membership


### Request

#### Endpoint

```plaintext
DELETE /api/v1/teams/17115/members/16793
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlNGQxYzI0MS0xNWU4LTQwMGYtYjA0ZS0xNjI2YzA5ZTJmYTAiLCJzdWIiOiIxNjUyNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNiwiZXhwIjoxNjA3NjQ1NzI2fQ.uJXMf6c5FzV6uDaF7FH7SO373QofnZ51cjmuou9leog
```

`DELETE /api/v1/teams/:id/members/:membership_id`

#### Parameters



| Name | Description |
|:-----|:------------|
| billing_admin *required* | User must be a billing admin |
| user_id *required* |  user |
| role  | user or billing_admin |
| licensed  | boolean |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/teams/17115/members/16793" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlNGQxYzI0MS0xNWU4LTQwMGYtYjA0ZS0xNjI2YzA5ZTJmYTAiLCJzdWIiOiIxNjUyNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNiwiZXhwIjoxNjA3NjQ1NzI2fQ.uJXMf6c5FzV6uDaF7FH7SO373QofnZ51cjmuou9leog"
```
## List team memberships


### Request

#### Endpoint

```plaintext
GET /api/v1/teams/17111/members
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxMWI5ZTA5YS1mYzQ5LTQzNTYtOGM1Ny1jN2E5NDAxOGQ1MjMiLCJzdWIiOiIxNjUyMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNSwiZXhwIjoxNjA3NjQ1NzI1fQ.AC_jzld6WO8BNhJ3kz3s4Up_Sv_3Jkf-rey_NKQUvmg
```

`GET /api/v1/teams/:id/members`

#### Parameters



| Name | Description |
|:-----|:------------|
| billing_admin *required* | User must be a billing admin |
| user_id *required* |  user |
| role  | user or billing_admin |
| licensed  | boolean |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "16785",
      "type": "memberships",
      "attributes": {
        "user_id": 16522,
        "role": "billing_admin",
        "name": "Arclight Mr Titan",
        "email": "vickie@jakubowski-bernhard.name",
        "licensed": true,
        "profile_image": "http://harber.info/leo"
      }
    },
    {
      "id": "16787",
      "type": "memberships",
      "attributes": {
        "user_id": 16523,
        "role": "billing_admin",
        "name": "Ultron Supah Quantum Eyes",
        "email": "test1@test.com",
        "licensed": true,
        "profile_image": "http://strosin.net/sidney.maggio"
      }
    }
  ],
  "meta": {
    "member_count": 2,
    "licensed_member_count": 2
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/teams/17111/members" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxMWI5ZTA5YS1mYzQ5LTQzNTYtOGM1Ny1jN2E5NDAxOGQ1MjMiLCJzdWIiOiIxNjUyMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNSwiZXhwIjoxNjA3NjQ1NzI1fQ.AC_jzld6WO8BNhJ3kz3s4Up_Sv_3Jkf-rey_NKQUvmg"
```
## Update membership


### Request

#### Endpoint

```plaintext
PUT /api/v1/teams/17113/members/16790
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzZjU5ZDZlNy1iMjVjLTRmMzQtOWJmOC02MDA3NjUzMzBlYzYiLCJzdWIiOiIxNjUyNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNiwiZXhwIjoxNjA3NjQ1NzI2fQ.5353AkyGbx-Bey431BszzfZLz5nf-YGC8oX10xsuTGo
```

`PUT /api/v1/teams/:id/members/:membership_id`

#### Parameters


```json
{"data":{"type":"team","attributes":{"role":"billing_admin","licensed":true}}}
```


| Name | Description |
|:-----|:------------|
| billing_admin *required* | User must be a billing admin |
| user_id *required* |  user |
| role  | user or billing_admin |
| licensed  | boolean |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "16790",
    "type": "memberships",
    "attributes": {
      "user_id": 16525,
      "role": "billing_admin",
      "name": "Cyborg Predator Dragon Giant Kool-Aid Man",
      "email": "test1@test.com",
      "licensed": true,
      "profile_image": "http://jacobi.info/kali"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/teams/17113/members/16790" -d '{"data":{"type":"team","attributes":{"role":"billing_admin","licensed":true}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzZjU5ZDZlNy1iMjVjLTRmMzQtOWJmOC02MDA3NjUzMzBlYzYiLCJzdWIiOiIxNjUyNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNiwiZXhwIjoxNjA3NjQ1NzI2fQ.5353AkyGbx-Bey431BszzfZLz5nf-YGC8oX10xsuTGo"
```
# Teams

Update team attributes or evaluation settings

## List teams


### Request

#### Endpoint

```plaintext
GET /api/v1/teams
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkZGZlZTI0NC01OWE4LTQyYTQtYjZjNC04ZjE5YjRkM2FhODkiLCJzdWIiOiIxNjYxMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.t2g-g58hYOLXcjeoW1FiCI35u_cUw0QEK_5UlEGd0_Y
```

`GET /api/v1/teams`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "17204",
      "type": "teams",
      "attributes": {
        "name": "mraz",
        "image": null,
        "domain": "mraz.name",
        "license_by": "domain",
        "current_user_membership": {
          "id": 16879,
          "user_id": 16613,
          "created_at": "2020-11-16T00:15:38.900Z",
          "updated_at": "2020-11-16T00:15:38.900Z",
          "role": "billing_admin",
          "team_id": 17204,
          "licensed": true
        },
        "domains_allowlist": null
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/teams" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkZGZlZTI0NC01OWE4LTQyYTQtYjZjNC04ZjE5YjRkM2FhODkiLCJzdWIiOiIxNjYxMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.t2g-g58hYOLXcjeoW1FiCI35u_cUw0QEK_5UlEGd0_Y"
```
## Show team


### Request

#### Endpoint

```plaintext
GET /api/v1/teams/17203
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjYTlmYzFjZS04Y2JlLTQwMmYtODg3ZS01MDkzYTg1ZTcyY2QiLCJzdWIiOiIxNjYxMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.tpDGZWePc5EiGt6c8N0kFxas2CPQ1xBsDbE9hcR3wXo
```

`GET /api/v1/teams/:id`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "17203",
    "type": "teams",
    "attributes": {
      "name": "ortiz-smitham",
      "image": null,
      "domain": "ortiz-smitham.biz",
      "license_by": "domain",
      "current_user_membership": {
        "id": 16878,
        "user_id": 16612,
        "created_at": "2020-11-16T00:15:38.772Z",
        "updated_at": "2020-11-16T00:15:38.772Z",
        "role": "billing_admin",
        "team_id": 17203,
        "licensed": true
      },
      "domains_allowlist": null
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/teams/17203" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjYTlmYzFjZS04Y2JlLTQwMmYtODg3ZS01MDkzYTg1ZTcyY2QiLCJzdWIiOiIxNjYxMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.tpDGZWePc5EiGt6c8N0kFxas2CPQ1xBsDbE9hcR3wXo"
```
## Update team


### Request

#### Endpoint

```plaintext
PUT /api/v1/teams/17202
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1NWY4MmI1Mi03OTY1LTRkYmYtYTJhNS04ODM5MmFiMDk5YzMiLCJzdWIiOiIxNjYxMSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.o4KcVSiDvFHqvALlplBoMHdGS35N1PMCORVPUBKB8Xs
```

`PUT /api/v1/teams/:id`

#### Parameters


```json
{"data":{"type":"team","attributes":{"required_category":true,"required_agenda":true,"license_by":"invite","annual_salary":220000}}}
```


| Name | Description |
|:-----|:------------|
| billing_admin *required* | User must be a billing admin |
| evaluation_setting  |  evaluation setting |
| action_setting  |  action setting |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "17202",
    "type": "teams",
    "attributes": {
      "name": "towne",
      "image": null,
      "domain": "towne.com",
      "license_by": "invite",
      "current_user_membership": {
        "id": 16877,
        "user_id": 16611,
        "created_at": "2020-11-16T00:15:38.618Z",
        "updated_at": "2020-11-16T00:15:38.618Z",
        "role": "billing_admin",
        "team_id": 17202,
        "licensed": true
      },
      "domains_allowlist": null
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/teams/17202" -d '{"data":{"type":"team","attributes":{"required_category":true,"required_agenda":true,"license_by":"invite","annual_salary":220000}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1NWY4MmI1Mi03OTY1LTRkYmYtYTJhNS04ODM5MmFiMDk5YzMiLCJzdWIiOiIxNjYxMSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.o4KcVSiDvFHqvALlplBoMHdGS35N1PMCORVPUBKB8Xs"
```
# Tips



## Clear all tips for user


### Request

#### Endpoint

```plaintext
DELETE /api/v1/tips/all
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyOTQxMmNlYS1kNzVmLTQ3NTQtYjQxNi1iZjM4NjA3MGE1NzUiLCJzdWIiOiIxNjYwNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.KKDb6fv6fKTFxhyFnKwRejug5w577_1heMxX4UQlk2I
```

`DELETE /api/v1/tips/all`

#### Parameters


None known.


### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/tips/all" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyOTQxMmNlYS1kNzVmLTQ3NTQtYjQxNi1iZjM4NjA3MGE1NzUiLCJzdWIiOiIxNjYwNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.KKDb6fv6fKTFxhyFnKwRejug5w577_1heMxX4UQlk2I"
```
## Flag tip as seen for user


### Request

#### Endpoint

```plaintext
PUT /api/v1/tips/5
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MTVkMzE0OC01YmY3LTQzNTAtYjg5ZS1kYWIzNTJmY2RhZDIiLCJzdWIiOiIxNjYwNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNywiZXhwIjoxNjA3NjQ1NzM3fQ.jsBFqcfsIw5NLXiDQrBsks524oJR-k-syS_Xgt9T93c
```

`PUT /api/v1/tips/:id`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "5",
    "type": "tip",
    "attributes": {
      "title": "Balance",
      "description": "Featuring your meeting preferences that are pre-optimized based on research from meeting experts.",
      "tag": "view-balance",
      "seen_at": "2020-11-16T00:15:37.969Z"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/tips/5" -d '' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MTVkMzE0OC01YmY3LTQzNTAtYjg5ZS1kYWIzNTJmY2RhZDIiLCJzdWIiOiIxNjYwNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczNywiZXhwIjoxNjA3NjQ1NzM3fQ.jsBFqcfsIw5NLXiDQrBsks524oJR-k-syS_Xgt9T93c"
```
## List tips for user


### Request

#### Endpoint

```plaintext
GET /api/v1/tips
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkYmY5YTVmNi1lZjRmLTRkNTEtYWY3Ny0wNzhlNzNkODMyZWMiLCJzdWIiOiIxNjYwNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.ABzWByU-2we4kWF27Y_QTlb_Wz6-a0qB_OcyzK2ycMA
```

`GET /api/v1/tips`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "1",
      "type": "tip",
      "attributes": {
        "title": "Add info from your calendar!",
        "description": "Agenda items and objectives can be added from the description in your meeting invite in Google or Outlook. We will organize it nicely for you!",
        "tag": "agenda-parser",
        "seen_at": null
      }
    },
    {
      "id": "2",
      "type": "tip",
      "attributes": {
        "title": "Auto-Balance",
        "description": "By default, MeetWell automatically interacts with meeting invites that stray from your preferences. You’ll receive an email before any action is taken. This is where the REAL (time-saving) magic happens.",
        "tag": "non-compliance-action",
        "seen_at": null
      }
    },
    {
      "id": "3",
      "type": "tip",
      "attributes": {
        "title": "Review",
        "description": "This view allows you to monitor yours and/or your team's overall meeting health and behaviors during any stretch of time.",
        "tag": "view-review",
        "seen_at": null
      }
    },
    {
      "id": "4",
      "type": "tip",
      "attributes": {
        "title": "Plan",
        "description": "This view features your week at a glance, and more!",
        "tag": "view-plan",
        "seen_at": null
      }
    },
    {
      "id": "5",
      "type": "tip",
      "attributes": {
        "title": "Balance",
        "description": "Featuring your meeting preferences that are pre-optimized based on research from meeting experts.",
        "tag": "view-balance",
        "seen_at": null
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/tips" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkYmY5YTVmNi1lZjRmLTRkNTEtYWY3Ny0wNzhlNzNkODMyZWMiLCJzdWIiOiIxNjYwNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.ABzWByU-2we4kWF27Y_QTlb_Wz6-a0qB_OcyzK2ycMA"
```
# User Settings

Update user action or evaluation settings

## Show settings progress


### Request

#### Endpoint

```plaintext
GET /api/v1/users/settings/progress?by_period[starts_at]=2020-11-16+00%3A15%3A20+UTC&amp;by_period[ends_at]=2020-11-23+00%3A15%3A20+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3OTQ1N2FmNy05MDFkLTRmOWMtOWVjNy02ZDY3YmFiN2EyNWEiLCJzdWIiOiIxNjQ5MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMCwiZXhwIjoxNjA3NjQ1NzIwfQ.J6Rn1zaATdMyCrcbed7URGjbVt1PlOzAFjblCwKEyOc
```

`GET /api/v1/users/settings/progress`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-11-16 00:15:20 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-23 00:15:20 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "80",
      "type": "settings_versions",
      "attributes": {
        "id": 80,
        "date": "2020-11-16T00:15:20.455Z"
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/users/settings/progress?by_period[starts_at]=2020-11-16+00%3A15%3A20+UTC&by_period[ends_at]=2020-11-23+00%3A15%3A20+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3OTQ1N2FmNy05MDFkLTRmOWMtOWVjNy02ZDY3YmFiN2EyNWEiLCJzdWIiOiIxNjQ5MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMCwiZXhwIjoxNjA3NjQ1NzIwfQ.J6Rn1zaATdMyCrcbed7URGjbVt1PlOzAFjblCwKEyOc"
```
## Show user settings


### Request

#### Endpoint

```plaintext
GET /api/v1/users/settings
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNzU3NTE4Yi01OWZhLTRjZWYtOTdhNC01ZDg1ZGY4Zjc1MjQiLCJzdWIiOiIxNjQ4OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMCwiZXhwIjoxNjA3NjQ1NzIwfQ.jehgFFUquhGLk92z9XoQi_eHCLO7gTDwcadkji8XiFE
```

`GET /api/v1/users/settings`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "16489",
    "type": "user_settings",
    "attributes": {
      "action_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "non_compliance_action": "remind",
        "domains_allowlist": "lubowitz-kozey.com",
        "last_minute_schedule": 6,
        "compliance_deadline": 6,
        "max_attendees": 12,
        "desired_duration": 90,
        "required_agenda": true,
        "required_category": false,
        "required_intention": false,
        "required_objectives": false,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false
      },
      "default_action_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "non_compliance_action": "remind",
        "domains_allowlist": null,
        "last_minute_schedule": 6,
        "compliance_deadline": 6,
        "max_attendees": 12,
        "desired_duration": 90,
        "required_agenda": true,
        "required_category": false,
        "required_intention": false,
        "required_objectives": false,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false
      },
      "evaluation_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "last_minute_schedule": 24,
        "max_attendees": 8,
        "desired_duration": 45,
        "required_agenda": true,
        "required_category": false,
        "required_intention": true,
        "required_objectives": true,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false,
        "ignore_all_day_meetings": true,
        "ignore_all_hands_meetings": true,
        "annual_salary": 75000
      },
      "default_evaluation_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "last_minute_schedule": 24,
        "max_attendees": 8,
        "desired_duration": 45,
        "required_agenda": true,
        "required_category": false,
        "required_intention": true,
        "required_objectives": true,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false,
        "ignore_all_day_meetings": true,
        "ignore_all_hands_meetings": true,
        "annual_salary": 75000
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/users/settings" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNzU3NTE4Yi01OWZhLTRjZWYtOTdhNC01ZDg1ZGY4Zjc1MjQiLCJzdWIiOiIxNjQ4OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMCwiZXhwIjoxNjA3NjQ1NzIwfQ.jehgFFUquhGLk92z9XoQi_eHCLO7gTDwcadkji8XiFE"
```
## Update user settings


### Request

#### Endpoint

```plaintext
PUT /api/v1/users/settings
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1ZmMwNjY0YS0xMWFjLTRiZTYtYjVkMi1hM2JhOTgyYzU2ZDciLCJzdWIiOiIxNjQ4OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMCwiZXhwIjoxNjA3NjQ1NzIwfQ.Mwt8dop9Uo_PxV39Y3YeaNPaYfP4ZP3vIBQuyQ0YT-c
```

`PUT /api/v1/users/settings`

#### Parameters


```json
{"data":{"type":"team","attributes":{"action_settings":{"required_agenda":false,"desired_duration":60,"last_minute_schedule":6},"evaluation_settings":{"max_attendees":8}}}}
```


| Name | Description |
|:-----|:------------|
| evaluation_setting  |  evaluation setting |
| action_setting  |  action setting |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "16488",
    "type": "user_settings",
    "attributes": {
      "action_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "non_compliance_action": "remind",
        "domains_allowlist": "lemke.org",
        "last_minute_schedule": 6,
        "compliance_deadline": 6,
        "max_attendees": 12,
        "desired_duration": 60,
        "required_agenda": false,
        "required_category": false,
        "required_intention": false,
        "required_objectives": false,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false
      },
      "default_action_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "non_compliance_action": "remind",
        "domains_allowlist": null,
        "last_minute_schedule": 6,
        "compliance_deadline": 6,
        "max_attendees": 12,
        "desired_duration": 90,
        "required_agenda": true,
        "required_category": false,
        "required_intention": false,
        "required_objectives": false,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false
      },
      "evaluation_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "last_minute_schedule": 24,
        "max_attendees": 8,
        "desired_duration": 45,
        "required_agenda": true,
        "required_category": false,
        "required_intention": true,
        "required_objectives": true,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false,
        "ignore_all_day_meetings": true,
        "ignore_all_hands_meetings": true,
        "annual_salary": 75000
      },
      "default_evaluation_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "last_minute_schedule": 24,
        "max_attendees": 8,
        "desired_duration": 45,
        "required_agenda": true,
        "required_category": false,
        "required_intention": true,
        "required_objectives": true,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false,
        "ignore_all_day_meetings": true,
        "ignore_all_hands_meetings": true,
        "annual_salary": 75000
      }
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/users/settings" -d '{"data":{"type":"team","attributes":{"action_settings":{"required_agenda":false,"desired_duration":60,"last_minute_schedule":6},"evaluation_settings":{"max_attendees":8}}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1ZmMwNjY0YS0xMWFjLTRiZTYtYjVkMi1hM2JhOTgyYzU2ZDciLCJzdWIiOiIxNjQ4OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyMCwiZXhwIjoxNjA3NjQ1NzIwfQ.Mwt8dop9Uo_PxV39Y3YeaNPaYfP4ZP3vIBQuyQ0YT-c"
```
# Users

Update user attributes or evaluation settings

## Delete user account and all associated data


### Request

#### Endpoint

```plaintext
DELETE /api/v1/users
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0YTRiYzQzZi01YTliLTRlNzEtODgwOS1jZjA4NWJmMDI3ZTEiLCJzdWIiOiIxNjYxMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.DjsixJxWdTAQ9arJSvyHXIwVcX50S43nwPXkC1U3ojM
```

`DELETE /api/v1/users`

#### Parameters


None known.


### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/users" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0YTRiYzQzZi01YTliLTRlNzEtODgwOS1jZjA4NWJmMDI3ZTEiLCJzdWIiOiIxNjYxMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.DjsixJxWdTAQ9arJSvyHXIwVcX50S43nwPXkC1U3ojM"
```
## Show user


### Request

#### Endpoint

```plaintext
GET /api/v1/users
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3MjlmNTFiMi0xNzg1LTQ1Y2UtYjFmMS1mM2VkZmNiMjcxMGYiLCJzdWIiOiIxNjYwOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.CCGb56sXza3dIRWMLq0mgnuMipz7_7QVUIik_XL7ioM
```

`GET /api/v1/users`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "16609",
    "type": "users",
    "attributes": {
      "email": "valentin@green.org",
      "domain": "green.org",
      "first_name": "Multiple",
      "last_name": "Atom",
      "profile_image": "http://wilkinson-strosin.io/paris",
      "time_zone": "UTC",
      "onboarded": false,
      "identity_providers": [

      ],
      "subscription_plan": null,
      "daily_report_card_events": true,
      "company": {
        "id": 17200,
        "name": "green",
        "license_by": "domain",
        "roles": [
          "billing_admin"
        ],
        "domains_allowlist": null,
        "organizer_denylist": ""
      },
      "organizer_denylist": "",
      "domains_allowlist": "green.org",
      "communication_prefs": {
        "all_communications": "pre_and_post",
        "email_tips": true,
        "email_weekly_reports": true,
        "email_reminders": "pre_and_post"
      },
      "goal_ids": [

      ]
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/users" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3MjlmNTFiMi0xNzg1LTQ1Y2UtYjFmMS1mM2VkZmNiMjcxMGYiLCJzdWIiOiIxNjYwOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.CCGb56sXza3dIRWMLq0mgnuMipz7_7QVUIik_XL7ioM"
```
## Update user


### Request

#### Endpoint

```plaintext
PUT /api/v1/users
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0OWJjOTM1ZS0yMzkyLTQ3MWEtOTc3Yy01ZmRhNjQ3NjI2YTAiLCJzdWIiOiIxNjYwOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.mdTOm8hWtEnhbkg1oVMiOnK_eU2a_QuVwa2_JwK1fKc
```

`PUT /api/v1/users`

#### Parameters


```json
{"communication_prefs":{"email_reminders":"pre_and_post","all_communications":true,"email_tips":true,"email_weekly_reports":true},"data":{"type":"team","attributes":{"required_category":true,"required_agenda":true,"annual_salary":220000}}}
```


| Name | Description |
|:-----|:------------|
| evaluation_setting  |  evaluation setting |
| action_setting  |  action setting |
| communication_prefs  |  communication prefs |
| communications_prefs[all_communications]  | True value sets all prefs to true |
| communications_prefs[email_tips]  | Ex: onboarding emails |
| communications_prefs[email_reminders]  | no_email, pre_and_post, pre_action, post_action |
| communications_prefs[email_weekly_reports]  | Communications prefs email weekly reports |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "16608",
    "type": "users",
    "attributes": {
      "email": "francisco@hettinger.biz",
      "domain": "hettinger.biz",
      "first_name": "Cyborg Forge",
      "last_name": "Magnificent Gorilla Grodd Wolf",
      "profile_image": "http://halvorson.co/tonja_kulas",
      "time_zone": "UTC",
      "onboarded": false,
      "identity_providers": [

      ],
      "subscription_plan": null,
      "daily_report_card_events": true,
      "company": {
        "id": 17199,
        "name": "hettinger",
        "license_by": "domain",
        "roles": [
          "billing_admin"
        ],
        "domains_allowlist": null,
        "organizer_denylist": ""
      },
      "organizer_denylist": "",
      "domains_allowlist": "hettinger.biz",
      "communication_prefs": {
        "all_communications": "pre_and_post",
        "email_tips": true,
        "email_weekly_reports": true,
        "email_reminders": "pre_and_post"
      },
      "goal_ids": [

      ]
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/users" -d '{"communication_prefs":{"email_reminders":"pre_and_post","all_communications":true,"email_tips":true,"email_weekly_reports":true},"data":{"type":"team","attributes":{"required_category":true,"required_agenda":true,"annual_salary":220000}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0OWJjOTM1ZS0yMzkyLTQ3MWEtOTc3Yy01ZmRhNjQ3NjI2YTAiLCJzdWIiOiIxNjYwOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTczOCwiZXhwIjoxNjA3NjQ1NzM4fQ.mdTOm8hWtEnhbkg1oVMiOnK_eU2a_QuVwa2_JwK1fKc"
```
# Wellness Blocks



## Create focus block


### Request

#### Endpoint

```plaintext
POST /api/v1/focus_blocks
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1MDc3NjEwNi1kODE1LTQ4NzYtOTYwYi02ZjkzYjRlMmU2YWEiLCJzdWIiOiIxNjUzNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNywiZXhwIjoxNjA3NjQ1NzI3fQ.GnTWv07lgLIUpOLTlshz39dA7fkwndx9LDmWA1BC_v0
```

`POST /api/v1/focus_blocks`

#### Parameters


```json
{"data":{"type":"focus_block","attributes":{"label":"Coding MeetWell","calendar_id":18941,"rrule":"DTSTART;TZID=PST:20191228T140357\nRRULE:FREQ=WEEKLY;BYDAY=MO,TU,WE,FR,SA","starts_at":"2019-12-28 22:03:57 UTC","ends_at":"2019-12-28 23:03:57 UTC"}}}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "657",
    "type": "focus_blocks",
    "attributes": {
      "label": "Coding MeetWell",
      "category": "focus",
      "calendar_id": 18941,
      "recurring_meeting_uuid": null,
      "duration": 3600,
      "starts_at": "2020-11-09T22:03:00.000Z",
      "ends_at": "2020-11-09T23:03:00.000Z",
      "rrule": "RRULE:FREQ=WEEKLY;BYDAY=MO,TU,WE,FR,SA",
      "recurring": true
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/focus_blocks" -d '{"data":{"type":"focus_block","attributes":{"label":"Coding MeetWell","calendar_id":18941,"rrule":"DTSTART;TZID=PST:20191228T140357\nRRULE:FREQ=WEEKLY;BYDAY=MO,TU,WE,FR,SA","starts_at":"2019-12-28 22:03:57 UTC","ends_at":"2019-12-28 23:03:57 UTC"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1MDc3NjEwNi1kODE1LTQ4NzYtOTYwYi02ZjkzYjRlMmU2YWEiLCJzdWIiOiIxNjUzNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNywiZXhwIjoxNjA3NjQ1NzI3fQ.GnTWv07lgLIUpOLTlshz39dA7fkwndx9LDmWA1BC_v0"
```
## Delete wellness block


### Request

#### Endpoint

```plaintext
DELETE /api/v1/focus_blocks/658
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjZjFkM2QwNS1mM2FkLTRlMmEtOWEzMC02ZjNlZjdkMTFhMTIiLCJzdWIiOiIxNjUzNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNywiZXhwIjoxNjA3NjQ1NzI3fQ.YfwuNZaCSx7d3XJTcmgi2MkFXjAL-V-siALSi-CS10s
```

`DELETE /api/v1/focus_blocks/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/focus_blocks/658" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjZjFkM2QwNS1mM2FkLTRlMmEtOWEzMC02ZjNlZjdkMTFhMTIiLCJzdWIiOiIxNjUzNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNywiZXhwIjoxNjA3NjQ1NzI3fQ.YfwuNZaCSx7d3XJTcmgi2MkFXjAL-V-siALSi-CS10s"
```
## List maybe wellness blocks


### Request

#### Endpoint

```plaintext
GET /api/v1/focus_blocks/maybe
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2NTRmODUxZS1hYTVmLTQ2NzYtYWRlMi0yYzNmOWNjYjFlNGYiLCJzdWIiOiIxNjUzOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOCwiZXhwIjoxNjA3NjQ1NzI4fQ.OwSSon5f6P_MsbkxnDra6DFnQlLY9buOLoBbdyASapo
```

`GET /api/v1/focus_blocks/maybe`

#### Parameters



| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [

  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/focus_blocks/maybe" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2NTRmODUxZS1hYTVmLTQ2NzYtYWRlMi0yYzNmOWNjYjFlNGYiLCJzdWIiOiIxNjUzOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOCwiZXhwIjoxNjA3NjQ1NzI4fQ.OwSSon5f6P_MsbkxnDra6DFnQlLY9buOLoBbdyASapo"
```
## List wellness blocks


### Request

#### Endpoint

```plaintext
GET /api/v1/focus_blocks
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3YjFlYjUyNi1iYjI4LTQ4ZTctYjAwMy1jZWRiZjYxZjg3MjUiLCJzdWIiOiIxNjUzNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOCwiZXhwIjoxNjA3NjQ1NzI4fQ.MbxVYCmW0BBoVrFp-eyP-geLSXQSaG6UPjp1THZrN4A
```

`GET /api/v1/focus_blocks`

#### Parameters



| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "659",
      "type": "focus_blocks",
      "attributes": {
        "label": "test",
        "category": "focus",
        "calendar_id": 18943,
        "recurring_meeting_uuid": "foo",
        "duration": 3600,
        "starts_at": "2020-11-16T00:15:00.000Z",
        "ends_at": "2020-11-16T01:15:00.000Z",
        "rrule": "RRULE:FREQ=DAILY",
        "recurring": true
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/focus_blocks" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3YjFlYjUyNi1iYjI4LTQ4ZTctYjAwMy1jZWRiZjYxZjg3MjUiLCJzdWIiOiIxNjUzNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyOCwiZXhwIjoxNjA3NjQ1NzI4fQ.MbxVYCmW0BBoVrFp-eyP-geLSXQSaG6UPjp1THZrN4A"
```
## Show wellness blocks


### Request

#### Endpoint

```plaintext
GET /api/v1/focus_blocks/655
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNTRjMTcwMi1jYTEzLTRlNjMtOGM0MC1mNTE5ODBiY2M4ZjAiLCJzdWIiOiIxNjUzNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNywiZXhwIjoxNjA3NjQ1NzI3fQ.HoWt7lsAdoVfKoYPVg_EF4PtE_P7_lS9r4mJLKWD-o8
```

`GET /api/v1/focus_blocks/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "655",
    "type": "focus_blocks",
    "attributes": {
      "label": "test",
      "category": "focus",
      "calendar_id": 18940,
      "recurring_meeting_uuid": "foo",
      "duration": 3600,
      "starts_at": "2020-11-16T00:15:00.000Z",
      "ends_at": "2020-11-16T01:15:00.000Z",
      "rrule": "RRULE:FREQ=DAILY",
      "recurring": true
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/focus_blocks/655" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNTRjMTcwMi1jYTEzLTRlNjMtOGM0MC1mNTE5ODBiY2M4ZjAiLCJzdWIiOiIxNjUzNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNywiZXhwIjoxNjA3NjQ1NzI3fQ.HoWt7lsAdoVfKoYPVg_EF4PtE_P7_lS9r4mJLKWD-o8"
```
## Update wellness block


### Request

#### Endpoint

```plaintext
PUT /api/v1/focus_blocks/654
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlZjZmNWE0YS0zMDVjLTQ2YzItYTVhMC0zODFlNjJmZmI4OGQiLCJzdWIiOiIxNjUzMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNywiZXhwIjoxNjA3NjQ1NzI3fQ.Q_BaNpth8_c3HPjiCMyP4YQ9egSJHdZuQ3J3PBZBeOM
```

`PUT /api/v1/focus_blocks/:id`

#### Parameters


```json
{"data":{"type":"focus_block","attributes":{"label":"test","rrule":"DTSTART;TZID=PST:20191228T140357\nRRULE:FREQ=WEEKLY;BYDAY=FR,SA","duration":3600}}}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "654",
    "type": "focus_blocks",
    "attributes": {
      "label": "test",
      "category": "focus",
      "calendar_id": 18939,
      "recurring_meeting_uuid": "foo",
      "duration": 3600,
      "starts_at": "2020-11-13T00:15:00.000Z",
      "ends_at": "2020-11-13T01:15:00.000Z",
      "rrule": "RRULE:FREQ=WEEKLY;BYDAY=FR,SA",
      "recurring": true
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/focus_blocks/654" -d '{"data":{"type":"focus_block","attributes":{"label":"test","rrule":"DTSTART;TZID=PST:20191228T140357\nRRULE:FREQ=WEEKLY;BYDAY=FR,SA","duration":3600}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlZjZmNWE0YS0zMDVjLTQ2YzItYTVhMC0zODFlNjJmZmI4OGQiLCJzdWIiOiIxNjUzMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwNTQ4NTcyNywiZXhwIjoxNjA3NjQ1NzI3fQ.Q_BaNpth8_c3HPjiCMyP4YQ9egSJHdZuQ3J3PBZBeOM"
```
