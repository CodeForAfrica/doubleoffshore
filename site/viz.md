---
layout: page
title: Viz
permalink: /viz/
---
<div ng-controller="NetworkController as network" class="container-fluid">
    <div id="canvas" class="col-md-10"></div>
    <div class="pull-right col-md-2">
        <form ng-submit="network.createNetwork()">
            Show me rigs<br />in
            <select ng-model="currentLocation" ng-options="country for (country, rigs) in locations">
                <option value="">any country</option>
            </select>
            <br />that are owned by
            <select ng-model="currentCompany" ng-options="company for (company, rigs) in companies">
                <option value="">anyone</option>
            </select>
            <br />and sailing under
            <select ng-model="currentFlag" ng-options="flag for (flag, rigs) in flags">
                <option value="">any country</option>
            </select>
            <br/><input type="submit" class="btn btn-default" value="Show rigs" />
        </form>
    </div>
</div>

<script type="text/javascript" src="{{ "/assets/jquery/dist/jquery.min.js" | prepend: site.baseurl }}"></script>
<script type="text/javascript" src="{{ "/assets/angular/angular.min.js" | prepend: site.baseurl }}"></script>
<script type="text/javascript" src="{{ "/assets/d3/d3.min.js" | prepend: site.baseurl }}"></script>
<script type="text/javascript" src="{{ "/assets/webcola/WebCola/cola.v3.min.js" | prepend: site.baseurl }}"></script>
<script type="text/javascript" src="{{ "/assets/js/app.js" | prepend: site.baseurl }}"></script>