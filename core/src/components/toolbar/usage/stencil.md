```tsx
import { Component, h } from '@stencil/core';

@Component({
  tag: 'toolbar-example',
  styleUrl: 'toolbar-example.css'
})
export class ToolbarExample {

  clickedStar() {
    console.log("Clicked star button");
  }

  clickedSearch() {
    console.log("Clicked search button");
  }

  render() {
    return [
      <ion-toolbar>
        <ion-title>Title Only</ion-title>
      </ion-toolbar>,

      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-back-button></ion-back-button>
        </ion-buttons>
        <ion-title>Back Button</ion-title>
      </ion-toolbar>,

      <ion-toolbar>
        <ion-title size="small">Small Title above a Default Title</ion-title>
      </ion-toolbar>,
      <ion-toolbar>
        <ion-title>Default Title</ion-title>
      </ion-toolbar>,

      <ion-toolbar>
        <ion-buttons slot="secondary">
          <ion-button>
            <ion-icon slot="icon-only" name="person-circle"></ion-icon>
          </ion-button>
          <ion-button>
            <ion-icon slot="icon-only" name="search"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-buttons slot="primary">
          <ion-button color="secondary">
            <ion-icon slot="icon-only" ios="ellipsis-horizontal" md="ellipsis-vertical"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-title>Default Buttons</ion-title>
      </ion-toolbar>,

      <ion-toolbar>
        <ion-buttons slot="secondary">
          <ion-button fill="solid">
            <ion-icon slot="start" name="person-circle"></ion-icon>
            Contact
          </ion-button>
        </ion-buttons>
        <ion-title>Solid Buttons</ion-title>
        <ion-buttons slot="primary">
          <ion-button fill="solid" color="secondary">
            Help
            <ion-icon slot="end" name="help-circle"></ion-icon>
          </ion-button>
        </ion-buttons>
      </ion-toolbar>,

      <ion-toolbar>
        <ion-buttons slot="secondary">
          <ion-button fill="outline">
            <ion-icon slot="start" name="star"></ion-icon>
            Star
          </ion-button>
        </ion-buttons>
        <ion-title>Outline Buttons</ion-title>
        <ion-buttons slot="primary">
          <ion-button color="danger" fill="outline">
            Edit
            <ion-icon slot="end" name="create"></ion-icon>
          </ion-button>
        </ion-buttons>
      </ion-toolbar>,

      <ion-toolbar>
        <ion-buttons slot="secondary">
          <ion-button>
            Account
          </ion-button>
        </ion-buttons>
        <ion-buttons slot="primary">
          <ion-button color="danger">
            Edit
          </ion-button>
        </ion-buttons>
        <ion-title>Text Only Buttons</ion-title>
      </ion-toolbar>,

      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-menu-button autoHide={false}></ion-menu-button>

        </ion-buttons>
        <ion-buttons slot="secondary">
          <ion-button>
            <ion-icon slot="icon-only" name="star"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-title>Left side menu toggle</ion-title>
      </ion-toolbar>,

      <ion-toolbar>
        <ion-buttons slot="primary">
          <ion-button onClick={() => this.clickedStar()}>
            <ion-icon slot="icon-only" name="star"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-title>Right side menu toggle</ion-title>
        <ion-buttons slot="end">
          <ion-menu-button autoHide={false}></ion-menu-button>

        </ion-buttons>
      </ion-toolbar>,

      <ion-toolbar>
        <ion-buttons slot="primary">
          <ion-button onClick={() => this.clickedSearch()}>
            <ion-icon slot="icon-only" name="search"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-searchbar placeholder="Search Favorites"></ion-searchbar>
      </ion-toolbar>,

      <ion-toolbar>
        <ion-segment value="all">
          <ion-segment-button value="all">
            All
          </ion-segment-button>
          <ion-segment-button value="favorites">
            Favorites
          </ion-segment-button>
        </ion-segment>
      </ion-toolbar>,

      <ion-toolbar color="secondary">
        <ion-buttons slot="secondary">
          <ion-button>
            <ion-icon slot="icon-only" name="person-circle"></ion-icon>
          </ion-button>
          <ion-button>
            <ion-icon slot="icon-only" name="search"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-buttons slot="primary">
          <ion-button color="primary">
            <ion-icon slot="icon-only" ios="ellipsis-horizontal" md="ellipsis-vertical"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-title>Secondary Toolbar</ion-title>
      </ion-toolbar>,

      <ion-toolbar color="dark">
        <ion-buttons slot="secondary">
          <ion-button>
            <ion-icon slot="icon-only" name="person-circle"></ion-icon>
          </ion-button>
          <ion-button>
            <ion-icon slot="icon-only" name="search"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-buttons slot="primary">
          <ion-button color="danger">
            <ion-icon slot="icon-only" ios="ellipsis-horizontal" md="ellipsis-vertical"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-title>Dark Toolbar</ion-title>
      </ion-toolbar>
    ];
  }
}
```