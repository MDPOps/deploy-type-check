# Check DeployType by MDP

GitHub Action for Check DeployType

## Code

```
- name: Check DeployType by MDP              
  uses: MDPOps/deploy-type-check@v1
  with:
	deployHostPaths: 
	  ${{ inputs.deployHostPaths }}
  id: deploy-type-check
```



