# pathScan-match
pathScan 指纹库
```yaml
rules:
  - name: 'github-token'
    matchers:
      - type: regex
        part: body
        regex:
          - '\b((?:ghu|ghs)_[a-zA-Z0-9]{36})\b'
  - name: 'azure-key'
    matchers:
      - type: word
        part: body
        words:
          - ''Ocp-Apim-Subscription-Key':'
  - name: 'ali-key'
    matchers:
      - type: regex
        part: body
        regex:
          - (?i)\b((LTAI)(?i)[a-z0-9]{20})(?:['|\"|\n|\r|\s|\x60|;]|$)
          - (?i)(?:algolia)(?:[0-9a-z\-_\t .]{0,20})(?:[\s|']|[\s|"]){0,3}(?:=|>|:=|\|\|:|<=|=>|:)(?:'|\"|\s|=|\x60){0,5}([a-z0-9]{32})(?:['|\"|\n|\r|\s|\x60|;]|$)
          - (?i)(?:alibaba)(?:[0-9a-z\-_\t .]{0,20})(?:[\s|']|[\s|"]){0,3}(?:=|>|:=|\|\|:|<=|=>|:)(?:'|\"|\s|=|\x60){0,5}([a-z0-9]{30})(?:['|\"|\n|\r|\s|\x60|;]|$)
```