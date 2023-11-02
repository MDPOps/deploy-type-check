# Check DeployType by MDP

GitHub Action for Check DeployType

## Code

```
jobs:
  check:
    runs-on: ubuntu-latest
    steps:

      - name: Checkout GitHub Repository
        uses: actions/checkout@v4

      - name: Check DeployType by MDP              
        uses: MDPOps/deploy-type-check@v1
        id: deploy-type-check

      - name: deploy-type-hosts
        shell: bash
        run: |
          echo ${{ steps.deploy-type-check.outputs.deployType }}
        if: steps.deploy-type-check.outputs.deployType == 'hosts'

      - name: deploy-type-apps
        shell: bash
        run: |
          echo ${{ steps.deploy-type-check.outputs.deployType }}
        if: steps.deploy-type-check.outputs.deployType == 'apps'
```



