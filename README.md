<h1>CodeIgniter y el MVC</h1>


<p><b>Herramientas empleadas:</b> La herramienta principal sera Codeigniter, apoyandose en bootstrap y jquery</p>


<p><b>Aplicacion a desarrollar:</b> La aplicacion a desarrollar sera una tienda online, utilizando unicamente codeigniter y sus librerias para demostrar su potencia respecto a otros frameworks.</p>

<img src="http://blog.collectivecloudperu.com/wp-content/uploads/2015/04/111.png">

<ul>
  <li>Que es CI</li>
  <li>Razones por las que usar CI como framework de desarrollo en seridor.</li>
  <li>Arquitectura MVC</li>
  <li>Pros y Contras del MVC</li>
  <li>Ventajas de usar CI</li>
  <li>Comparacion de CI frente a otros</li>
  <li>Cracteristicas y potencia de CI</li>
  <li>Clases y librerias de CI</li>
  <li>CI en la comunidad de desarrolladores</li>
  <li>CI como framework back mas utilizado</li>
  <li>Aplicacion de CI</li>
</ul>

<h3>Librerias utilizadas</h3>

Caching Driver

<pre><code>
En el ejemplo siguiente se carga el controlador de memoria caché, APC como driver a utilizar, y cambia a almacenamiento en caché basado en archivo si APC no está disponible en el entorno de alojamiento.
$this->load->driver('cache', array('adapter' => 'apc', 'backup' => 'file'));

if ( ! $foo = $this->cache->get('foo'))
{
        echo 'Saving to the cache!<br />';
        $foo = 'foobarbaz!';

        // Save into the cache for 5 minutes
        $this->cache->save('foo', $foo, 300);
}

echo $foo;
</code></pre>

Calendaring Class

<pre><code>
Agregar datos a las celdas de tu calendario involucra crear un arreglo asociativo en el cual los índices corresponden a los días que desea llenar y el valor del arreglo contiene los datos. El arreglo es pasado al tercer parámetro de la función generar calendario. Considere este ejemplo:
$this->load->library('calendar');

$data = array(
               3  => 'http://example.com/news/article/2006/03/',
               7  => 'http://example.com/news/article/2006/07/',
               13 => 'http://example.com/news/article/2006/13/',
               26 => 'http://example.com/news/article/2006/26/'
             );

echo $this->calendar->generate(2006, 6, $data);
</code></pre>


Shopping Cart Class
Para agregar un ítem al carrito, podemos utilizar un array multidimensional con la información del producto a la función $this- >cart->insert(), según se muestra aquí:
<pre><code>$data = array(
               array(
                       'id'      => 'sku_123ABC',
                       'qty'     => 1,
                       'price'   => 39.95,
                       'name'    => 'T-Shirt',
                       'options' => array('Size' => 'L', 'Color' => 'Red')
                    ),
               array(
                       'id'      => 'sku_567ZYX',
                       'qty'     => 1,
                       'price'   => 9.95,
                       'name'    => 'Coffee Mug'
                    ),
               array(
                       'id'      => 'sku_965QRS',
                       'qty'     => 1,
                       'price'   => 29.95,
                       'name'    => 'Shot Glass'
                    )
            );

$this->cart->insert($data);
</code></pre>

Config Class
Por defecto, CodeIgniter tiene un archivo primario de configuracion, ubicado en application/config/config.php. Si abres un archivo usando tu editor de texto verás que los items son almacenados en un arreglo llamado $config.

Puedes agregar tus propios items de configuración a este archivo, o si lo prefieres, puedes mantenerlos en forma separada (asumiendo que necesitas items de configuración), simplemente debes crear tu archivo de configuración y guardarlo en la carpeta config.

<pre><code>$this->config->load('nombre_archivo')</code></pre>

Email Class

Encrypt Class
Encryption Library
File Uploading Class
Form Validation
FTP Class
Image Manipulation Class
Input Class
Javascript Class
Language Class
Loader Class
Output Class
Pagination Class
Template Parser Class
Security Class
Session Library
HTML Table Class
Trackback Class
Typography Class
Unit Testing Class
URI Class
User Agent Class
XML-RPC and XML-RPC Server Classes
Zip Encoding Class

