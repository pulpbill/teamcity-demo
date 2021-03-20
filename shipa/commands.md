### Connect to shipa target
`shipa target-add shipa $SHIPA_HOST -s`

`shipa login nn@nn.com`

### User Role Permission

#### list command 
`shipa node-list`

`shipa role-list`

`shipa user-list`

`shipa permission-list`

#### show users with their roles
`shipa user-list`

#### Create role with team context
`shipa role-add developer team`

#### Add permissions to the role
`shipa role-permission-add developer app cluster.read framework.read framework.update`

#### Assign the role to a user and user to team "shipa-dev-team"
`shipa role-assign developer developer@nn.com shipa-dev-team`

`shipa user-list`

#### remove role 
`shipa role-remove developer`


### Deploy application in shipa framework
`shipa app-create my-app --team shipa-dev-team --framework development`

`shipa app-deploy --app my-app -i nginx`

`shipa app log -a app-name`





