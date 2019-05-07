ember-tab-menu
==============================================================================

This is a simple addon which adds a basic tab menu component. Using the currentTab variable you can show different blocks of your application depending on which of your tabs is currently selected.


Compatibility
------------------------------------------------------------------------------

* Ember.js v2.18 or above
* Ember CLI v2.13 or above


Installation
------------------------------------------------------------------------------

```
ember install ember-tab-menu
```


Usage
------------------------------------------------------------------------------

Ember addon adds a simple tab menu component. You can create as many tabs as you wish. The currentTab will return the name of the currentTab or the Id if it is passed through to the item. You can also pass through the ```currentWhen``` or ```params```  which will be passed this through to a linkTo in the component. If you do not have ```currentWhen``` added it will revert back and use the ```name``` to determine which tab is currently selected. 

The addon can be used for showing different sub routes through the use of currentWhen and params. 

```
<TabMenu @currentTab=currentTab as |tm|>

    {{tm.item name='Menu 1' currentWhen='index.pageone' params=params}}
    {{tm.item name='Menu 2' currentWhen='index.pagetwo' params=params}}
    {{tm.item name='Menu 3' currentWhen='index.pagethree' params=params}}

</TabMenu>
```


Contributing
------------------------------------------------------------------------------

See the [Contributing](CONTRIBUTING.md) guide for details.


License
------------------------------------------------------------------------------

This project is licensed under the [MIT License](LICENSE.md).
