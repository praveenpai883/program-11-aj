<!DOCTYPE html>
<html>
<head>
 <title>Student Details</title>
 <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.8.2/angular.min.js"></script>
</head>
<body ng-app="myApp">
 <h1>Student Details</h1>
 <table>
 <thead>
 <tr>
 <th>Name</th>
 <th>CGPA</th>
 </tr>
 </thead>
 <tbody>
 <tr ng-repeat="student in students">
 <td>{{student.name | uppercase}}</td>
 <td>{{student.cgpa}}</td>
 </tr>
 </tbody>
 </table>
<script src= “P11.js”></script>
</body>
</html>
P11.js
angular.module('myApp', []).controller('appCtrl', function($scope) {
 $scope.students = [
 { name: "John Doe", cgpa: 3.8 },
 { name: "Jane Doe", cgpa: 3.6 },
 { name: "Peter Parker", cgpa: 3.9 },
 { name: "Mary Jane Watson", cgpa: 3.7 }
 ];
});
