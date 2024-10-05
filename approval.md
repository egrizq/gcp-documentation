# Approvals

## POST /approvals/request

Request Body
```json
{
  "vehicle": string 
  "driver": string
  "destination": string
  "date": string
  "approvel": string
}
```

Response Body (Success)
```json
{
  "status_code": 201
  "message": "Request registered successfully"
}
```

Response Body (Failed)
```json
{
  "status_code": 400
  "message": "Invalid input data: some fields cannot be empty"
}
```

## POST /approvals/:id/approve

Response Body (Success)
```json
{
  "status_code": 200
  "message": "Approval successful"
}
```

Response Body (Failed)
```json
{
  "status_code": 400
  "message": "Invalid id: request rejected"
}
```

## POST /approvals/:id/reject

Response Body (Success)
```json
{
  "status_code": 200
  "message": "Rejection successful"
}
```

Response Body (Failed)
```json
{
  "status_code": 400
  "message": "Invalid id: request rejected"
}
```

## GET /approvals/history?status

Response Body (Success)
```json
{
  "status_code": 200
  "data": [
    {
        "booking_id": int,
        "vehicle": string,
        "driver": string,
        "destination": string
        "status": "approved" | "rejected",
        "date": string
        "requestor": string,
    }
  ]
}
```

Response Body (Failed)

Invalid Status Query
```json
{
  "status_code": 404
  "message": "Invalid status parameter. Allowed values are 'approved' or 'rejected'."
}
```

No Records Found:
```json
{
  "status_code": 404
  "message": "No approval history found for the given status."
}
```
