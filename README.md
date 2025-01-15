# Traffic System Controller for Unity  

![TrafficSystem Example](Media/GIF1%20-%20README.gif)  
*An example.*

A Unity solution for simulating basic traffic behavior using waypoints. This system is designed for simplicity, making it ideal for quick prototypes or basic traffic implementations.

## Features  
- **Waypoint-Based Movement**: Vehicles move along predefined paths using waypoints.  
- **Dynamic Route Selection**: Vehicles randomly choose paths at intersections.  
- **Collision Avoidance**: Vehicles detect and stop for others using raycasting.  
- **Customizable Speed and Behavior**: Configure vehicle speed, detection range, and stopping thresholds.  
- **Visual Debugging**: Waypoint connections are displayed in the scene view with Gizmos and labels for easy setup.

## Installation  
1. Download the [`TrafficSystemController.unitypackage`](TrafficSystemController.unitypackage) file from this repository.  
2. Open your Unity project and go to **Assets > Import Package > Custom Package**.  
3. Select the `TrafficSystemController.unitypackage` file and click **Import**.  

## How to Use  
1. **Setup Waypoints**:  
   - Add `WaypointController` to GameObjects in your scene.  
   - Link waypoints by assigning `nextWaypoints` in the Inspector to define paths.  

2. **Add Vehicles**:  
   - Attach the `VehicleController` script to your vehicle prefabs.  
   - Assign the first `WaypointController` to the `currentWaypoint` property in the Inspector.  
   - Specify the tag for vehicles (e.g., `Car`) in the `vehicleTag` field to enable collision detection.  

3. **Customize Behavior**:  
   - Adjust vehicle speed, raycast distance, and stop time thresholds in the Inspector.  
   - Set `nextWaypoints` for waypoints to control traffic flow.  

4. **Test Your Setup**:  
   - Play the scene and observe vehicles navigating the waypoints.  
   - Use Gizmos in the Scene view to visualize waypoint connections and debug traffic paths.

## Visual Debugging  
- Waypoints are connected by green lines.  
- Blue spheres indicate the location of each waypoint.  
- Arrowheads show the direction of the paths, making it easier to identify connections in the Scene view.  

## Example Usage  
1. Place waypoints in a road network to define vehicle paths.  
2. Add vehicles and configure their initial waypoints and movement parameters.  
3. Vehicles will follow the waypoints, handle intersections dynamically, and stop for other vehicles when needed.

## Limitations  
- Designed for simple traffic systems. More advanced behaviors (e.g., traffic lights) are not included.  
- Ensure waypoints are properly connected; disconnected waypoints will halt vehicle movement.  

## License  
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.  
