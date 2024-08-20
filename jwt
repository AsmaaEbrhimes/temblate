import { Component } from '@angular/core';
import { TranslateService } from "@ngx-translate/core";
import * as jwt_decode from 'jwt-decode';
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  phoneNumber: any;
  token: string = '';
  ngOnInit(){
    this.GetToken()
  }
  constructor(private translate: TranslateService) {
    translate.setDefaultLang('en');
    translate.use('en');
  }

  useLanguage(language: string): void {
    this.translate.use(language);
  }

  GetToken() {
    this.token = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMDEwNjUxNTQzNzMiLCJqdGkiOiJmOGE4M2NkNy1kNjk1LTQ4ODQtOTQ5ZS1kMmJlY2UxNWUxY2UiLCJ1aWQiOiJlM2JmYWM0Yi1hMjdiLTRjZWItYmE2Yy04YmIzMTk5ZmIwYjciLCJCcmFuc2giOiI0NGY2ZDhmYy04NTI5LTRhODAtOWY5My0wOGRjYmM2YmZhOWQiLCJUZW5hbnRJZCI6ImQ1NGNkOTY5LTliOWYtNGMwNy05NDZkLTRmNTlkYzY4ZmZhYyIsIkNvbXBhbnlJRCI6IjI4MjkwNzMwLWNhODktNGI4Ny1hZTY1LTA4ZGNiYzZiZmExMiIsIlVzZXJOYW1lIjoiMDExODg4ODg4ODgiLCJjb21wYW55bmFtZSI6IiIsImh0dHA6Ly9zY2hlbWFzLnhtbHNvYXAub3JnL3dzLzIwMDUvMDUvaWRlbnRpdHkvY2xhaW1zL25hbWVpZGVudGlmaWVyIjoiZTNiZmFjNGItYTI3Yi00Y2ViLWJhNmMtOGJiMzE5OWZiMGI3IiwiaHR0cDovL3NjaGVtYXMubWljcm9zb2Z0LmNvbS93cy8yMDA4LzA2L2lkZW50aXR5L2NsYWltcy9yb2xlIjoiVXNlciIsImV4cCI6MTcyNDE0NDE4OCwiaXNzIjoiaHR0cDovL2xvY2FsaG9zdDo1MDAwIiwiYXVkIjoiaHR0cDovL2xvY2FsaG9zdDo0MjAwIn0.rv4XSxeIFq_Z6EdiQMS3KwzxxUxTE7LLNenFBZ_DFJw&id=MfTkvjBpAtgXhDDXPRstJg.';
    const decodedToken: any = jwt_decode.jwtDecode(this.token);
    const userRole = decodedToken['http://schemas.microsoft.com/ws/2008/06/identity/claims/role'];
    console.log('User Role:', userRole);
    if (userRole == 'User') {
      console.log('hello')
    }
  }


}








