import { Component, ViewChild } from '@angular/core';
import { Nav, Platform } from 'ionic-angular';
import { StatusBar } from '@ionic-native/status-bar';
import { SplashScreen } from '@ionic-native/splash-screen';

import { TabsPage } from '../pages/tabs/tabs';
import { LoginPage } from '../pages/login/login';
//push
//import { Push, PushToken } from '@ionic/cloud-angular';
import { HomePage } from '../pages/home/home';
import { CalendarPage } from '../pages/calendar/calendar';
import { NoticeListPage } from '../pages/notice/noticeList';
import { MyPage } from '../pages/myPage/myPage';


@Component({
  templateUrl: 'app.html'
})
export class MyApp {
  @ViewChild(Nav) nav: Nav;
  
  // rootPage:any = TabsPage;
  rootPage : any = LoginPage;

  pages: Array<{title: string, name: string, component: any, tabComponent?: any, index? : number;}>;
  constructor(public platform: Platform, public statusBar: StatusBar, public splashScreen: SplashScreen) {
    // 메뉴바 이동을 위한 페이지 설정
    this.pages = [
      { title: 'Home', name: 'TabsPage', component: TabsPage, tabComponent: HomePage, index : 0 },
      { title: 'Notice', name: 'TabsPage', component: TabsPage, tabComponent: NoticeListPage, index : 1 },
      { title: 'Calendar', name: 'TabsPage', component: TabsPage, tabComponent: CalendarPage, index : 2 },
      { title: 'MyPage', name: 'TabsPage', component: TabsPage, tabComponent: MyPage, index : 3}
    ];
    this.intializeApp();
  }

  // 앱 시작
  intializeApp(){
    this.platform.ready().then(() => {    
      this.statusBar.styleDefault();
      this.splashScreen.hide();
      /* this.platform.registerBackButtonAction(()=>{
        let view = this.nav.getActive();
        if (view.component.name == "LoginPage") {
          this.platform.exitApp();
          // event.preventDefault();
        } 
        // else if(view.component.name == "CalendarModifyModalPage" || view.component.name == "CalendarViewModalPage" || view.component.name == "CalendarWriteModalPage"){
        //   this.nav.pop({});
        // } 
        else {
          this.nav._app.goBack();
          // this.nav.canGoBack();
        }

        // if (this.nav.canGoBack()) {
        //   this.nav.pop();
        //   }
        //   else {
        //   this.platform.exitApp();  //This step can be handled further as per requirement
        //   }
      }) */
    });
  }

  // 메뉴바 클릭시 해당 페이지 이동 이벤트
  openPage(page) {
    // Reset the content nav to have just this page
    // we wouldn't want the back button to show in this scenario
    let params = {};

    if(page.index){
      params = {tabIndex: page.index};
    }

    this.nav.setRoot(page.component, params);
    // this.nav.push(page.component);
    // this.nav.setRoot(TabsPage.prototype.tab4Root);
  }

  // 로그아웃
  logout(){
    this.nav.setRoot(LoginPage);
  }
}
