# redireccion.github.io

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="utf-8" />
    <title>Redirigiendo a la tienda...</title>
    <script>
    function getMobileOperatingSystem() {
      var userAgent = navigator.userAgent || navigator.vendor || window.opera;

      // Windows Phone primero, ya que su UA incluye "Android"
      if (/windows phone/i.test(userAgent)) {
          return "Windows Phone";
      }

      if (/android/i.test(userAgent)) {
          return "Android";
      }

      // Detección de iOS
      if (/iPad|iPhone|iPod/.test(userAgent) && !window.MSStream) {
          return "iOS";
      }

      return "unknown";
    }

    function DetectAndServe() {
        let os = getMobileOperatingSystem();
        if (os == "Android") {
            window.location.href = "https://play.google.com/store/apps/details?id=com.ficohsa.activities";  // Reemplaza con tu enlace de Play Store
        } else if (os == "iOS") {
            window.location.href = "https://apps.apple.com/gt/app/ficohsa/id474591239";  // Reemplaza con tu enlace de App Store
        } else {
            window.location.href = "https://secure.ficohsa.com";  // Fallback para otros dispositivos (ej. PC)
        }
    }
    </script>
</head>
<body onload="DetectAndServe()">
    <p>Redirigiendo automáticamente...</p>
</body>
</html>
