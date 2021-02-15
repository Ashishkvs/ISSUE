#install json-server
#npm install -g json-server
---------

json-server public/swiggy-server.json --port 3000


-------------------------------
# remove header and footer based on url
<app-header-one [sticky]="true" *ngIf="url != '/pages/comingsoon'"></app-header-one>
<router-outlet></router-outlet>
<app-footer-one *ngIf="url != '/pages/comingsoon'"></app-footer-one>

------------------------------------
public url : any; 

  constructor(private router: Router) {  
    this.router.events.subscribe((event) => {
          if (event instanceof NavigationEnd) {
            this.url = event.url;
          }
    });
  }
  
  # end 
