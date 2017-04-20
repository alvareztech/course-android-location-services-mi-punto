# Mi Punto En El Mundo Real

Ejemplo de aplicación para obtener la localización.

## Para completar la aplicación

1. Implementar en la activity principal `LocationListener` y su método `onLocationChanged(...)`

2. Colocar el siguiente código para iniciar el proceso de obtención de actualizaciones 

```java
LocationRequest locationRequest = new LocationRequest();
locationRequest.setInterval(1000);
locationRequest.setPriority(LocationRequest.PRIORITY_HIGH_ACCURACY);
LocationServices.FusedLocationApi.requestLocationUpdates(googleApiClient, locationRequest, this);
```

3. Colocar el siguiente código dentro del método `onLocationChanged(...)`

```java
Log.i("MIAPP", "Localización: " + location.getLatitude() + ", " + location.getLatitude());
latitudTextView.setText(String.valueOf(location.getLatitude()));
longitudTextView.setText(String.valueOf(location.getLongitude()));
```
