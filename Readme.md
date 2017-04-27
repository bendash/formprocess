# Formprocess #

## Notice ###

This extension is no longer maintained. If you are looking for an alternative, upgrade to TYPO3 v8 or use powermail.

## What does it do? ##

This extension offers the opportunity to define a custom Post Processor for the TYPO3 form system extension.
It also completely integrates itself into the TYPO3 Form Wizard.

## Users Manual ##

 1. Install Extension
 2. Create a form using the wizard
 3. Add the Post Processer 'User' to the form
 4. Define your User Function, for Example '\Vendor\Procuct\Utility\UserFunctions->myUserFunction'
 
The PostProcessor will pass two arguments to the user function, the first argument holds the submitted form data, the second argument is a reference to itself.
The User Function must accept these two arguments, for example:

```sh
public function myUserFunction($formData, &$pObj) {
  ... custom processing of form data
}
```
