# Hilbert Convolution

## Background

This project began with an interest in the idea of a hilbert curve to convert geographic and/or geospatial data. The problem with reducing geospatial data (and dimensionality reduction in general) is that information is lost, particularly, there is an increasing disconnect along the hilbert curve number line where quadrant boundaries exist (points along the boundary between first and last quadrants are directly next to each other in 2d space, but far apart along the number line). This project seeks to explore ways to preserve that information, such that n-dimensional objects may benefit from a hilbert transformation.

## Concept

The idea of the hilbert convolution was to calculate and sum the absolute distances along the line from each nearby point in 2d space, and graph those convolutions according to each point along the hilbert curve line. The resulting graph may present some interesting patterns that could be used to preserve the information lost by the hilbert transformation.

## Current State

The graph has been completed, though several things remain unclear:
1. Whether the convolution should be square (or circular, with points within some radius r having a 1.0 weight and those outside having a 0.0 weight)
2. The size of the convolution (a larger size evens out the graph, but may have unexpected side effects)
3. Useful properties of the graph

Currently, the graph does present some intuitive information about hilbert curves in general. Higher convolution scores tend to correlate with closeness to a boundary, though they do not discriminate by quadrant.

Additionally, the graph does maintain the fractal nature of hilbert curves, which is an interesting fact to explore.

## Future Developments
1. Graphing higher-dimensional hilbert convolutions
2. Transforming convolution scores (applying natural log, squared distances instead of absolute, etc.)
3. Dissecting quadrant data (and how to present/store it in a meaningful way)


