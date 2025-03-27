# Module based

**ngIf**

`<p *ngIf="serverCreated">Server was created, server name is {{ serverName }}</p>`

**else**

```
<p *ngIf="serverCreated; else noServer">Server was created, server name is {{ serverName }}</p>
<ng-template #noServer>
    <p>No server was created!</p>
</ng-template>
```

<hr>

**ngStyle**

`<p [ngStyle]="{backgroundColor: getColor()}">Server with ID {{ serverId }} is {{ getServerStatus() }}</p>`

```
getColor() {
    return this.serverStatus === 'online' ? 'green' : 'red';
  }
```

<hr>

**ngClass**

`<p [ngStyle]="{backgroundColor: getColor()}" [ngClass]="{online: serverStatus === 'online'}">Server with ID {{ serverId }} is {{ getServerStatus() }}</p>`

**ngFor**

`<app-server *ngFor="let server of servers" />`
