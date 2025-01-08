# Defold HC
Defold bindings for HardonCollider.

# Installation
You can use Defold HC in your own project by adding this project as a [Defold library dependency](http://www.defold.com/manuals/libraries/). Open your game.project file and in the dependencies field under project add:

    https://github.com/totebo/defold-hc/archive/master.zip

Or point to the ZIP file of a [specific release](https://github.com/totebo/defold-hc/releases).

## Example

    local HC = require "hc.hardoncollider"
    
    local collider = HC.new()
    
    function init(self)
    
    	local ball = collider:circle(100, 100, 20)
    	local rect = collider:rectangle(110, 90, 20, 100)
    
    	for shape, delta in pairs(collider:collisions(ball)) do
    	    shape:move(delta.x, delta.y)
    	end
    
    end

Refer to Hardon Collider reference for usage:

https://hc.readthedocs.io/en/latest/

https://github.com/vrld/HC
