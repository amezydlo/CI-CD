# CI-CD

on events:
- push
- pull_request
- create - branch or tag created
- fork
- issues - issue opened / closed
- issue_comment
- watch - repo starred
- discussion
- workflow_dispatch - manually trigger
- repository_dispatch - REST API request to trigger workflow
- schedule - workflow is scheduled
- workflow_call - another workflow calls this one

## Checkout the code:
```yaml
steps:
      - name: Get code
        uses: actions/checkout@v3
        with: <place here some action-specific settings>
```

By default jobs run in parallel...


CI could be skipped for instance when I only post new comment by pushing a commit with message including one of:
- [skip ci]
- [ci skip]
- [no ci]
- [skip actions]
- [actions skip]