# angular-risk-matrix, fork de estudo

> Fork oficial do projeto [JoeHogan/angular-risk-matrix](https://github.com/JoeHogan/angular-risk-matrix).

Este repositório é mantido apenas como referência de estudo. O código e a documentação original pertencem a Joe Hogan e aos respectivos contribuidores. Não há, neste momento, alterações autorais relevantes de Alan Nogueira.

A documentação original do projeto é preservada abaixo.

---

# angular-risk-matrix
A simple Risk Matrix chart for AngularJS

### Demo

http://jsfiddle.net/joehogan/5gzfeysv/10/

### Installation

Include the JS and CSS files for the plugin:

```
<link href="css/angular-risk-matrix.min.css" rel="stylesheet">
<script src="js/angular-risk-matrix.min.js"></script>
```

Add the module dependency in your AngularJS app:

```
angular.module('myModule', ['riskMatrix']);
```

### Usage

#### Basic

```
<risk-matrix data="data.risks" likelihood="data.likelihoodValues" impact="data.impactValues"></risk-matrix>
```

#### Attributes

##### Required

###### data

An array of your risk data objects with the following property structure, at a minimum:

```javascript
$scope.data.risks = [
    {
        Id: 1,
        RiskLikelihood: 'High',
        RiskImpact: 'Low'
    },
    {
        Id: 2,
        RiskLikelihood: 'Medium',
        RiskImpact: 'High'
    },
    {
        Id: 3,
        RiskLikelihood: 'Low',
        RiskImpact: 'Very High'
    },
    {
        Id: 4,
        RiskLikelihood: 'Very High',
        RiskImpact: 'Very High'
    }
];
```

###### likelihood

An array of five likelihood values from low to high corresponding with your data:

```javascript
$scope.data.likelihoodValues = [
    'Very Low', 'Low', 'Medium', 'High', 'Very High'
];
```

###### impact

An array of five impact values from low to high corresponding with your data:

```javascript
$scope.data.impactValues = [
    'Very Low', 'Low', 'Medium', 'High', 'Very High'
];
```

##### Optional

###### template

You can define a template string that will be compiled. Use `item` to refer to the current risk item:

```html
<risk-matrix
  data="data.risks"
  likelihood="data.likelihoodValues"
  impact="data.impactValues"
  template="data.riskTemplate">
</risk-matrix>
```

Original template example: http://jsfiddle.net/joehogan/6xqkwf8p/3/
