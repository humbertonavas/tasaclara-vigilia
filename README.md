# Vigilia de Tasa Clara

Vigilancia externa de [Tasa Clara](https://tasaclara.socialwebseo.com), la app informativa y gratuita de
tasas de cambio en Venezuela.

Cada 10 minutos, este repositorio llama al vigilante del sitio (`/push/salud.php`), que:

- reinstala la tarea programada del servidor si el hosting la borró;
- relanza la actualización de tasas si los datos tienen más de 12 minutos.

Si las tasas llevan más de 30 minutos sin actualizarse, o las divisas del mundo más de 6 horas, la
ejecución falla y GitHub avisa por correo a quien mantiene el repositorio.

No contiene secretos: solo consulta una dirección pública. Un «latido» mensual evita que GitHub apague
la tarea programada por inactividad.
