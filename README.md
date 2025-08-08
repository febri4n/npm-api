# npm-api
Manage Nginx Proxy Manager with API

```bash
curl -X POST https://example.com/api/tokens \
  -H "Content-Type: application/json" \
  -d '{"identity": "username@gmail.com", "secret": "SECRET"}' \
  | jq -r '.token' > npm_token.txt
```
```bash
curl -s -X GET https://example.com/api/nginx/proxy-hosts \
  -H "Authorization: Bearer $(cat npm_token.txt)" | jq
```
```bash
curl -s -X GET https://example.com/api/nginx/redirection-hosts \
  -H "Authorization: Bearer $(cat npm_token.txt)" | jq
```
```bash
curl -s -X GET https://example.com/api/nginx/certificates \
  -H "Authorization: Bearer $(cat npm_token.txt)" | jq
```
```bash
curl -s -X GET https://example.com/api/nginx/access-lists \
  -H "Authorization: Bearer $(cat npm_token.txt)" | jq
```
```bash
curl -s -X GET https://example.com/api/users \
  -H "Authorization: Bearer $(cat npm_token.txt)" | jq
```
