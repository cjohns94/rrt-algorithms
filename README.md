#Personal Notes
-pip install rtree didn't work for me, but sudo apt install python3-rtree did.

	This is the error message that came with pip install:
	Command "python setup.py egg_info" failed with error code 1 in /tmp/pip-build-541ysx/rtree/
-the pip install commands for dependencies all need to be pip3. (this still didnt work for rtree), but it did for the others. 

# rrt
Collection of rrt-based algorithms that scale to n-dimensions
- rrt
- rrt* (rrt-star)

## Requirements
- [Python 3+](https://www.python.org/downloads/)
- [NumPy](http://www.numpy.org/)
- [Rtree](https://pypi.python.org/pypi/Rtree/)
- [Plotly](https://plot.ly/python/getting-started/) (only needed for plotting)

## Usage
Define an n-dimensional Search Space, and n-dimensional obstacles within that space. Assign start and goal locations as well as the number of iterations to expand the tree before testing for connectivity with the goal, and the max number of overall iterations.

### Search Space
Assign bounds to Search Space in form: `[(x_lower, x_upper), (y_lower, y_upper), ...]`

### Start and Goal
Points represented by tuples of form: `(x, y, ...)`

### Obstacles
Axis-aligned (hyper)rectangles represented by a tuples of form `(x_lower, y_lower, ..., x_upper, y_upper, ...)`

Non-axis aligned (hyper)rectangles or other obstacle representations should also work, provided that `collision_free` and `obstacle_free` are updated to work with the new obstacles.

### Resolution
Assign resolution of edges:
- `q`: Distance away from existing vertices to probe.
- `r`: Discretization length to use for edges when sampling along them to check for collisions. Higher numbers run faster, but may lead to undetected collisions.

### Examples
Visualization examples can be found for rrt and rrt* in both 2 and 3 dimensions.
- [2D RRT](https://plot.ly/~szanlongo/79/plot/)
- [3D RRT](https://plot.ly/~szanlongo/81/plot/)
- [2D RRT*](https://plot.ly/~szanlongo/83/plot/)
- [3D RRT*](https://plot.ly/~szanlongo/89/plot/)
- [2D Bidirectional RRT*](https://plot.ly/~szanlongo/85/plot/)
- [3D Bidirectional RRT*](https://plot.ly/~szanlongo/87/plot/)
- [2D Heuristic Bidirectional RRT*](https://plot.ly/~szanlongo/91/plot/)
- [3D Heuristic Bidirectional RRT*](https://plot.ly/~szanlongo/93/plot/)

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

[MIT License](https://github.com/motion-planning/rrt-algorithms/blob/master/LICENSE)
