# Mi Punto En El Mundo Real

Ejemplo de aplicación para obtener actulizaciones de localización.

> Para abrir este proyecto puedes utilizar la siguiente opción en Android Studio.

<img width="468" alt="android-studio" src="https://cloud.githubusercontent.com/assets/1444991/25249559/48cf969e-25e0-11e7-915d-a98f77613462.png">

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
