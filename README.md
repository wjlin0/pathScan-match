# pathScan-match
pathScan 指纹库
```yaml
name: azure-oss
request:
  - method: GET
    path:
      - /
matchers:
  - type: regex
    part: header
    name: azure
    group: 1
    regex:
      - '(?i)Server: .*?(Windows-Azure-Blob[/\d\.]*).*?'
```