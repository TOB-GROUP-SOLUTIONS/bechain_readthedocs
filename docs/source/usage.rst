Integración
=====

.. _installation:

Aspectos Generales
------------

ARQUITECTURA REST

La API para desarrolladores de PAGOS360 utiliza una arquitectura REST.
URLs previsibles y orientadas a recursos, que utilizan códigos de respuesta HTTP para indicar errores. Funciones HTTP integradas, como la autenticación y los verbos, que son conocidos por los clientes estándares.

Autenticación
----------------

Para utilizar la plataforma se debe solicitar un token de acceso por sesión. Para esto debe enviar usuario y contraseña al endpoint de login para obtener el token.
Este token luego será enviado en la cabecera de cada llamado a la API.

.. code-block:: console

   /url.api.al.login

Certificaciones
----------------

Para realizar certificaciones (stamps) de documentos, datos o hashes en blockchain, se debe utilizar el endpoint "stamp". Se pueden enviar: documentos, un json con información o hashes.

Se obtendrá como respuesta el resultado del stamp sobre la blockchain.

.. code-block:: console

   /url.api.al.stamp

Validaciones
----------------

Para realizar validaciones de documentos, datos o hashes ya certificados en blockchain, se debe utilizar el endpoint "verify". Se pueden enviar: documentos, un json con información o hashes.

Se obtendrá como respuesta el resultado de la verificación sobre la blockchain.

.. code-block:: console

   /url.api.al.verify
















.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']

