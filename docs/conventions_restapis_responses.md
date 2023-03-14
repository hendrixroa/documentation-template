# RestAPI responses

Once the RestAPI design has been made, a convention schema response should be documented how you respond when the frontend or mobile team is calling you.

## Responses

## Success

Success: HTTP 2xx 
On success API returns following structure:
```ts
{
  data: { /* response data */ }
}
```

## Pagination

By convention paginated endpoints return data in following format:
```ts
{
  data: {
    results: [/* array of posts for example */],
    metadata: {
      pages: number,
      page: number,
      total: number,
    },
    ...anyAdditionalFieldsIfNeeded
  }
}
```

## Error

Error: HTTP 4xx/5xx 
On error API returns following structure:
```ts
{
  error: {
    message: 'Error message',
    details: [
      { path: '<field_path>', message: 'Field error message', reason: '<reasonCode>' },
      ...
    ],
    severity: 'error' | 'warning',
    type: 'authentication' | 'validation' | 'internal',
  }
}
```