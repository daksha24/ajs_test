# ajs_test

<!DOCTYPE html>
<html>
<script src="http://ajax.googleapis.com/ajax/libs/angularjs/1.4.8/angular.min.js"></script>
<body>

<div ng-app="myApp" ng-controller="myCtrl">

<p>Select a below options:</p>

<select ng-model="selectedValue">
<option ng-repeat="x in options" value="{{x.opt}}">{{x.opt}}</option>
</select>

<h2>You selected: {{selectedValue}}</h2>

</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
    $scope.options = [
        {opt : "post"},
        {opt : "user"},
        {opt : "new post"}
    ];
});
</script>


</body>
</html>
