### nav-view tab explain
the back button will be shown if <ion-nav-view> has a history. 
In tab, we have a <ion-nav-view> nested in higher <ion-nav-view>, 
the tab switching histtory will not be stacked on each other since it is the inner <ion-nav-view>.

- --<ion-nav-view> replaced
  - --<ion-nav-view>  stacked
  
### Install cordova camera plugin
Don't use the ionic plugin in the video that does not work
```shell
cordova plugin add cordova-plugin-camera
```

### View cahcing 
The account controller is cahced by default, but this is not good. 
If we made modification without saving, we can see it is still empty. If 
we want this name to be refreshed by data in AuthService. 
We simply need to add cache: false in account state.

```javascript
.state('tab.account', {
      url: '/account',
      views: {
        'tab-account': {
          templateUrl: 'templates/tabs/tab-account.html',
          controller: 'AccountCtrl',
        }
      },
      cache: false
    });

```
