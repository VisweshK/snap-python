GetNodeInDegV
'''''''''''''''

.. function:: GetNodeInDegV(Graph, NIdInDegV)

Computes the in-degree for every node in *Graph*. 
The result is stored in *NIdInDegV*, a vector of pairs (node id, node in degree).

Parameters:

- *Graph*: graph (input)
	A Snap.py graph or a network

- *NIdInDegV*: TIntPrV, a vector or (int, int) pairs (output)
	A vecotr of (node id, node in degree) pairs.

Return value:

- None

The following example shows how to use :func:`GetNodeInDegV` with nodes in :class:`TNGraph`, :class:`TUNGraph`, and :class:`TNEANet`::

    import snap

    Graph = snap.GenRndGnm(snap.PNGraph, 100, 1000)
    NIdInDegV = snap.TIntPrV()

    snap.GetNodeInDegV(Graph, NIdInDegV)

    for pair in NIdInDegV:
        print "Node id: %d, in-degree: %d" % (pair.GetVal1(), pair.GetVal2())

    Graph = snap.GenRndGnm(snap.PUNGraph, 100, 1000)
    NIdInDegV = snap.TIntPrV()

    snap.GetNodeInDegV(Graph, NIdInDegV)

    for pair in NIdInDegV:
        print "Node id: %d, in-degree: %d" % (pair.GetVal1(), pair.GetVal2())

    Graph = snap.GenRndGnm(snap.PNEANet, 100, 1000)
    NIdInDegV = snap.TIntPrV()

    snap.GetNodeInDegV(Graph, NIdInDegV)

    for pair in NIdInDegV:
        print "Node id: %d, in-degree: %d" % (pair.GetVal1(), pair.GetVal2())