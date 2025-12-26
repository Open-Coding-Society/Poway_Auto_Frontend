---
toc: true
layout: post
title: Traffic-Aware Route Finder
permalink: /route/
nav: true
---

<head>
  <link rel="stylesheet" type="text/css" href="{{site.baseurl}}/navigation/findBestRoute/map.css">
  <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />
</head>

<body>
  <!-- Page Header -->
  <div class="text-center mb-8">
    <span class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-primary-100 dark:bg-primary-900/30 text-primary-700 dark:text-primary-300 text-sm font-medium mb-4">
      <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
      </svg>
      Powered by San Diego Open Data
    </span>
  </div>

  <div class="route-form">
    <h2>🗺️ Traffic-Aware Route Finder</h2>
    <p style="font-size: 15px; color: #64748b;">
      Route estimates are dynamically adjusted using real traffic data from San Diego's official dataset.
    </p>
    <div class="input-group">
      <label for="origin">📍 Origin</label>
      <input type="text" id="origin" placeholder="Enter your starting point (e.g., Downtown San Diego)">
    </div>
    <div class="input-group">
      <label for="destination">🎯 Destination</label>
      <input type="text" id="destination" placeholder="Enter your destination (e.g., La Jolla Beach)">
    </div>
    <div class="input-group">
      <label for="mode">🚗 Travel Mode</label>
      <select id="mode">
        <option value="driving">🚗 Driving</option>
        <option value="walking">🚶 Walking</option>
        <option value="bicycling">🚴 Bicycling</option>
        <option value="transit">🚌 Transit</option>
      </select>
    </div>
    <button id="fetch_routes_btn">Find Best Route →</button>
  </div>

  <div id="map"></div>
  <div id="result"></div>

  <script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"></script>
  <script type="module" src="{{site.baseurl}}/navigation/findBestRoute/map.js"></script>
  <script type="module" src="{{site.baseurl}}/assets/js/api/config.js"></script>
</body>












