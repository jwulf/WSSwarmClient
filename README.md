# WSSwarmClient
Web sockets Swarm Client

Development:

        <script src="https://rawgit.com/salboaie/WSSwarmClient/master/src/SwarmDebug.js"></script>
        <script src="https://rawgit.com/salboaie/WSSwarmClient/master/src/SwarmClient.js"></script>
        <script src="https://rawgit.com/salboaie/WSSwarmClient/master/src/SwarmHub.js"></script>


Production

        <script src="https://cdn.rawgit.com/salboaie/WSSwarmClient/master/src/SwarmDebug.js"></script>
        <script src="https://cdn.rawgit.com/salboaie/WSSwarmClient/master/src/SwarmClient.js"></script>
        <script src="https://cdnrawgit.com/salboaie/WSSwarmClient/master/src/SwarmHub.js"></script>

## Example

```
 <script type="text/javascript">
            var client = new SwarmClient("localhost", 8080,
                "testUser", "ok", "testTenant", "testCtor",
                function securityErrorFunction(err){
                    alert(err);
                }, function errorFunction(err){
                alert(err);
            });
    
            swarmHub.resetConnection(client);
    
            swarmHub.on("login.js", "success", function(){
                alert("Test success")
            });
    
            swarmHub.on("login.js", "fail", function(){
                alert("Test failed")
            });
        </script>
```

```client = new SwarmClient(host, port, userId, authToken, tenantId, loginCtor, securityErrorFunction, errorFunction)```
