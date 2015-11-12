# VIPER convention

## Сontents

* [View](#view)
* [Interactor](#interactor)
  * [DataProvider](#dataprovider)
* [Presenter](#presenter)
* [Wireframe](#wireframe)
  * [Source](#source)

## View
_View layer_ includes ```UIViewController``` & ```UIView```.
For view events each subview should have weak link to the own delegate (usualy it's superview) and for the root view delegate should be ```UIViewController```. The view events delegate for ```UIViewController``` should be _Presenter layer_.

## Interactor
_Business layer_

### DataProvider
**Allowed:**
If Interactor's job is only get an Entities it's allowed to direct usage DataProvider instance without Interactor

## Presenter
_Presenter layer_ handle view events and know _when_ to navigate to other screen. _Presenter_ ask _wireframe_ to navigate to concreate screen. 

## Wireframe
_Wireframe_ know how to navigate to concreate screen.

### Source

