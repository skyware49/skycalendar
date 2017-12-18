import { Component } from '@angular/core';
import { NavParams, Platform, MenuController } from 'ionic-angular';
//import { AboutPage } from '../about/about';
import { MyPage } from '../myPage/myPage';
import { HomePage } from '../home/home';
import { CalendarPage } from '../calendar/calendar';
import { NoticeListPage } from '../notice/noticeList';
import { Http, Headers, RequestOptions } from '@angular/http';

// import { Http, Headers, RequestOptions } from '@angular/http';

@Component({
  selector: 'page-tabs',
  templateUrl: 'tabs.html'
})
export class TabsPage {

  tab1Root: any = HomePage;
  tab2Root: any = NoticeListPage;
  tab3Root: any = CalendarPage;
  tab4Root: any = MyPage;
  myIndex: number;

  constructor(navParams: NavParams, public platform: Platform, public menuCtrl: MenuController, private http: Http) {
    this.myIndex = navParams.data.tabIndex || 0;
    
    // document.addEventListener("backbutton", onBackKeyDown, false);
  
    // function onBackKeyDown(e){
    //   e.preventDefault();
    //   console.log("back키를 사용할 수 없습니다.")
    // }
    // platform.ready().then(() => {
    //   platform.registerBackButtonAction(() => {
        
    //   })
    // })
  }

  homeSelected(){
    console.log("탭눌러지냐?");
    HomePage.prototype.getWeekList(this.http);
    HomePage.prototype.getBirthList(this.http);
  }

}
