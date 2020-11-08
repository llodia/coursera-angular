# coursera-angular
Test coursera angular course

Angular Tutorial
https://www.toptal.com/angular-js/a-step-by-step-guide-to-your-first-angularjs-app
https://www.guru99.com/angularjs-tutorial.html

The first thing you’ll notice in this template is the use of expressions (“{{“ and “}}”) to return variable values. In AngularJS development, expressions allow you to execute some computation in order to return a desired value. Some valid expressions would be:
* {{ 1 + 1 }}
* {{ 946757880 | date }}
* {{ user.name }}
Effectively, expressions are JavaScript-like snippets. But despite being very powerful, you shouldn’t use expressions to implement any higher-level logic. For that, we use directives.

At a high level, directives are markers (such as attributes, tags, and class names) that tell AngularJS to attach a given behaviour to a DOM element (or transform it, replace it, etc.). L

https://www.toptal.com/angular-js/a-step-by-step-guide-to-your-first-angularjs-app

The ng-controller directive defines which controller will be in charge of your view. There is no view without controller

The ng-app directive is responsible for bootstrapping your app defining its scope. In AngularJS, you can have multiple apps within the same page, so this directive defines where each distinct app starts and ends.

The ng-app directive initializes an AngularJS application.

The ng-init directive initializes application data. =>Normally, you will not use ng-init. You will use a controller or module instead.

The ng-model directive binds the value of HTML controls (input, select, textarea) to application data.

The ng-model directive binds the value of HTML controls (input, select, textarea) to application data.


<ng-repeat ="x in name">

<script src='https://ajax.googleapis.com/ajax/libs/angularjs/1.6.4/angular.min.js'></script>



$scope variable we’re passing as a parameter to the controller. 
The $scope variable is supposed to link your controller and views. In particular, it holds all the data that will be used within your template. Anything you add to it (like the driversList in the above example) will be directly accessible in your views
The scope is a JavaScript object which basically binds the "controller" and the "view"
￼



￼


Module

An AngularJS module defines an application.
The module is a container for the different parts of an application.
The module is a container for the application controllers.
Controllers always belong to a module.

AngularJS controllers control the data of AngularJS applications.
AngularJS controllers are regular JavaScript Objects.


<div ng-app = “myApp”>….</div>
<script>

var app = angular.module(“myApp”, [] )

</script>


Adding a Controller
AngularJS controllers control the data of AngularJS applications.



￼




Add a controller to your application, and refer to the controller with the ng-controller directive:
<div ng-app =“myApp”  ng-controller=“myCtrl”>
{{ firstName + “ “ + lastName }}
</div>

<script>
var app = angular.module(“myApp”, []);
app.controller(“myCtrl”, function($scope)
{

 $scope.firstName = “David”;
 $scope.lastName  = “Diallo”;

});
</script>



Scope
The scope is the binding part between the HTML (view) and the JavaScript (controller).
The scope is an object with the available properties and methods.
The scope is available for both the view and the controller.
Modules are used to create that separation of boundaries and assist in separating controllers based on functionality.

When adding properties to the $scope object in the controller, the view (HTML) gets access to these properties.
In the view, you do not use the prefix $scope, you just refer to a propertyname, like {{carname}}.

<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.4/angular.min.js"></script>
<body>

<div ng-app="myApp" ng-controller="myCtrl">

<h1>{{carname}}</h1>

</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
    $scope.carname = "Volvo";
});
</script>

<p>The property "carname" was made in the controller, and can be referred to in the view by using the {{ }} brackets.</p>

</body>
</html>

