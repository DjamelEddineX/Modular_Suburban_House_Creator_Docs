Changelog
=========

1.0.0
-----
- Initial release
- No known bugs

1.0.1
-----
*Added*
- Added `_Openable` window and sliding window parts, better animation control and rendering use.

*Changed*
- The "Move" tool UI and tooltips now explicitly state movement is in Blender world axes (Left = -X, Right = +X, Front = -Y, Back = +Y, Up = +Z, Down = -Z).

*Fixed*
- When adding modular parts with multiple children, the true parent object is placed at the active object or cursor transform, not a random child. All children are unhidden and remain at correct relative positions.
- After duplicating a part (with children), only the new parent is selected and set active; children are not left selected.
- Improved icons logic.
- Delete operator now deletes only selected objects and their children, not the entire collection, unless the collection is empty.
- General code cleanup.

*Performance*
- Increased the speed of getting objects from the database (faster collection lookup and caching).
