Operation
=========

Categories
----------

This UI code creates movement controls:

.. code-block:: python

   move_col = tools_box.column(align=True)
   move_col.label(text="Move:")
   row = move_col.row(align=True)
   row.operator("object.move_part", text="← Left").direction = 'LEFT'
   row.operator("object.move_part", text="Right →").direction = 'RIGHT'
   row = move_col.row(align=True)
   row.operator("object.move_part", text="↑ Front").direction = 'FRONT'
   row.operator("object.move_part", text="↓ Back").direction = 'BACK'
   row = move_col.row(align=True)
   row.operator("object.move_part", text="↑ Up").direction = 'UP'
   row.operator("object.move_part", text="↓ Down").direction = 'DOWN'

- Creates a vertical column for movement controls
- Adds labeled buttons for left/right, front/back, and up/down movement
- Each button triggers the ``move_part`` operator with specific direction

Rotation Controls:

.. code-block:: python

   rotate_col = tools_box.column(align=True)
   rotate_col.label(text="Rotate:")
   row = rotate_col.row(align=True)
   row.operator("object.rotate_part", text="↺ -90°").angle = -90
   row.operator("object.rotate_part", text="↻ +90°").angle = 90

- Creates rotation buttons (-90° and +90°)
- Triggers ``rotate_part`` operator with angle parameter

Additional Tools:

.. code-block:: python

   row.operator("object.duplicate_part", text="Duplicate", icon='DUPLICATE')
   row.operator("object.delete_part", text="Delete", icon='TRASH')
   layout.operator("object.add_new_part", text="Create New Part", icon='ADD')

- Duplicate/Delete/New Part buttons with appropriate icons
