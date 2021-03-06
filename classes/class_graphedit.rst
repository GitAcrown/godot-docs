.. Generated automatically by doc/tools/makerst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the GraphEdit.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_GraphEdit:

GraphEdit
=========

**Inherits:** :ref:`Control<class_control>` **<** :ref:`CanvasItem<class_canvasitem>` **<** :ref:`Node<class_node>` **<** :ref:`Object<class_object>`

**Category:** Core

Brief Description
-----------------

GraphEdit is an area capable of showing various GraphNodes. It manages connection events between them.

Member Functions
----------------

+----------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`add_valid_connection_type<class_GraphEdit_add_valid_connection_type>` **(** :ref:`int<class_int>` from_type, :ref:`int<class_int>` to_type **)**                                                   |
+----------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`add_valid_left_disconnect_type<class_GraphEdit_add_valid_left_disconnect_type>` **(** :ref:`int<class_int>` type **)**                                                                             |
+----------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`add_valid_right_disconnect_type<class_GraphEdit_add_valid_right_disconnect_type>` **(** :ref:`int<class_int>` type **)**                                                                           |
+----------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`clear_connections<class_GraphEdit_clear_connections>` **(** **)**                                                                                                                                  |
+----------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Error<enum_@globalscope_error>`  | :ref:`connect_node<class_GraphEdit_connect_node>` **(** :ref:`String<class_string>` from, :ref:`int<class_int>` from_port, :ref:`String<class_string>` to, :ref:`int<class_int>` to_port **)**           |
+----------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`disconnect_node<class_GraphEdit_disconnect_node>` **(** :ref:`String<class_string>` from, :ref:`int<class_int>` from_port, :ref:`String<class_string>` to, :ref:`int<class_int>` to_port **)**     |
+----------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Array<class_array>`              | :ref:`get_connection_list<class_GraphEdit_get_connection_list>` **(** **)** const                                                                                                                        |
+----------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                | :ref:`is_node_connected<class_GraphEdit_is_node_connected>` **(** :ref:`String<class_string>` from, :ref:`int<class_int>` from_port, :ref:`String<class_string>` to, :ref:`int<class_int>` to_port **)** |
+----------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                | :ref:`is_valid_connection_type<class_GraphEdit_is_valid_connection_type>` **(** :ref:`int<class_int>` from_type, :ref:`int<class_int>` to_type **)** const                                               |
+----------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`remove_valid_connection_type<class_GraphEdit_remove_valid_connection_type>` **(** :ref:`int<class_int>` from_type, :ref:`int<class_int>` to_type **)**                                             |
+----------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`remove_valid_left_disconnect_type<class_GraphEdit_remove_valid_left_disconnect_type>` **(** :ref:`int<class_int>` type **)**                                                                       |
+----------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`remove_valid_right_disconnect_type<class_GraphEdit_remove_valid_right_disconnect_type>` **(** :ref:`int<class_int>` type **)**                                                                     |
+----------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`set_selected<class_GraphEdit_set_selected>` **(** :ref:`Node<class_node>` node **)**                                                                                                               |
+----------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Signals
-------

.. _class_GraphEdit__begin_node_move:

- **_begin_node_move** **(** **)**

Signal sent at the beginning of a GraphNode movement.

.. _class_GraphEdit__end_node_move:

- **_end_node_move** **(** **)**

Signal sent at the end of a GraphNode movement.

.. _class_GraphEdit_connection_request:

- **connection_request** **(** :ref:`String<class_string>` from, :ref:`int<class_int>` from_slot, :ref:`String<class_string>` to, :ref:`int<class_int>` to_slot **)**

Signal sent to the GraphEdit when the connection between 'from_slot' slot of 'from' GraphNode and 'to_slot' slot of 'to' GraphNode is attempted to be created.

.. _class_GraphEdit_connection_to_empty:

- **connection_to_empty** **(** :ref:`String<class_string>` from, :ref:`int<class_int>` from_slot, :ref:`Vector2<class_vector2>` release_position **)**

.. _class_GraphEdit_delete_nodes_request:

- **delete_nodes_request** **(** **)**

Signal sent when a GraphNode is attempted to be removed from the GraphEdit.

.. _class_GraphEdit_disconnection_request:

- **disconnection_request** **(** :ref:`String<class_string>` from, :ref:`int<class_int>` from_slot, :ref:`String<class_string>` to, :ref:`int<class_int>` to_slot **)**

Signal sent to the GraphEdit when the connection between 'from_slot' slot of 'from' GraphNode and 'to_slot' slot of 'to' GraphNode is attempted to be removed.

.. _class_GraphEdit_duplicate_nodes_request:

- **duplicate_nodes_request** **(** **)**

Signal sent when a GraphNode is attempted to be duplicated in the GraphEdit.

.. _class_GraphEdit_node_selected:

- **node_selected** **(** :ref:`Object<class_object>` node **)**

Emitted when a GraphNode is selected.

.. _class_GraphEdit_popup_request:

- **popup_request** **(** :ref:`Vector2<class_vector2>` p_position **)**

Signal sent when a popup is requested. Happens on right-clicking in the GraphEdit. 'p_position' is the position of the mouse pointer when the signal is sent.

.. _class_GraphEdit_scroll_offset_changed:

- **scroll_offset_changed** **(** :ref:`Vector2<class_vector2>` ofs **)**


Member Variables
----------------

  .. _class_GraphEdit_right_disconnects:

- :ref:`bool<class_bool>` **right_disconnects** - If ``true``, enables disconnection of existing connections in the GraphEdit by dragging the right end.

  .. _class_GraphEdit_scroll_offset:

- :ref:`Vector2<class_vector2>` **scroll_offset** - The scroll offset.

  .. _class_GraphEdit_snap_distance:

- :ref:`int<class_int>` **snap_distance** - The snapping distance in pixels.

  .. _class_GraphEdit_use_snap:

- :ref:`bool<class_bool>` **use_snap** - If ``true``, enables snapping.

  .. _class_GraphEdit_zoom:

- :ref:`float<class_float>` **zoom** - The current zoom value.


Description
-----------

GraphEdit manages the showing of GraphNodes it contains, as well as connections and disconnections between them. Signals are sent for each of these two events. Disconnection between GraphNodes slots is disabled by default.

It is greatly advised to enable low processor usage mode (see :ref:`OS.set_low_processor_usage_mode<class_OS_set_low_processor_usage_mode>`) when using GraphEdits.

Member Function Description
---------------------------

.. _class_GraphEdit_add_valid_connection_type:

- void **add_valid_connection_type** **(** :ref:`int<class_int>` from_type, :ref:`int<class_int>` to_type **)**

Makes possible the connection between two different slot types. The type is defined with the :ref:`GraphNode.set_slot<class_GraphNode_set_slot>` method.

.. _class_GraphEdit_add_valid_left_disconnect_type:

- void **add_valid_left_disconnect_type** **(** :ref:`int<class_int>` type **)**

Makes possible to disconnect nodes when dragging from the slot at the left if it has the specified type.

.. _class_GraphEdit_add_valid_right_disconnect_type:

- void **add_valid_right_disconnect_type** **(** :ref:`int<class_int>` type **)**

Makes possible to disconnect nodes when dragging from the slot at the right if it has the specified type.

.. _class_GraphEdit_clear_connections:

- void **clear_connections** **(** **)**

Remove all connections between nodes.

.. _class_GraphEdit_connect_node:

- :ref:`Error<enum_@globalscope_error>` **connect_node** **(** :ref:`String<class_string>` from, :ref:`int<class_int>` from_port, :ref:`String<class_string>` to, :ref:`int<class_int>` to_port **)**

Create a connection between 'from_port' slot of 'from' GraphNode and 'to_port' slot of 'to' GraphNode. If the connection already exists, no connection is created.

.. _class_GraphEdit_disconnect_node:

- void **disconnect_node** **(** :ref:`String<class_string>` from, :ref:`int<class_int>` from_port, :ref:`String<class_string>` to, :ref:`int<class_int>` to_port **)**

Remove the connection between 'from_port' slot of 'from' GraphNode and 'to_port' slot of 'to' GraphNode, if connection exists.

.. _class_GraphEdit_get_connection_list:

- :ref:`Array<class_array>` **get_connection_list** **(** **)** const

Return an Array containing the list of connections. A connection consists in a structure of the form {from_slot: 0, from: "GraphNode name 0", to_slot: 1, to: "GraphNode name 1" }

.. _class_GraphEdit_is_node_connected:

- :ref:`bool<class_bool>` **is_node_connected** **(** :ref:`String<class_string>` from, :ref:`int<class_int>` from_port, :ref:`String<class_string>` to, :ref:`int<class_int>` to_port **)**

Return true if the 'from_port' slot of 'from' GraphNode is connected to the 'to_port' slot of 'to' GraphNode.

.. _class_GraphEdit_is_valid_connection_type:

- :ref:`bool<class_bool>` **is_valid_connection_type** **(** :ref:`int<class_int>` from_type, :ref:`int<class_int>` to_type **)** const

Returns whether it's possible to connect slots of the specified types.

.. _class_GraphEdit_remove_valid_connection_type:

- void **remove_valid_connection_type** **(** :ref:`int<class_int>` from_type, :ref:`int<class_int>` to_type **)**

Makes it not possible to connect between two different slot types. The type is defined with the :ref:`GraphNode.set_slot<class_GraphNode_set_slot>` method.

.. _class_GraphEdit_remove_valid_left_disconnect_type:

- void **remove_valid_left_disconnect_type** **(** :ref:`int<class_int>` type **)**

Removes the possibility to disconnect nodes when dragging from the slot at the left if it has the specified type.

.. _class_GraphEdit_remove_valid_right_disconnect_type:

- void **remove_valid_right_disconnect_type** **(** :ref:`int<class_int>` type **)**

Removes the possibility to disconnect nodes when dragging from the slot at the right if it has the specified type.

.. _class_GraphEdit_set_selected:

- void **set_selected** **(** :ref:`Node<class_node>` node **)**

Sets the specified ``node`` as the one selected.


