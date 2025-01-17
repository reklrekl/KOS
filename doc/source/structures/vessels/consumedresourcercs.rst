.. _consumedresourcercs:

ConsumedResourceRCS
===================

A single resource value an rcs thruster consumes (i.e. monopropellant, etc). This is the type returned by the :struct:`RCS`:CONSUMEDRESOURCES suffix

.. structure:: ConsumedResourceRCS

    .. list-table::
        :header-rows: 1
        :widths: 2 1 4

        * - Suffix
          - Type
          - Description

        * - :attr:`NAME`
          - :struct:`String`
          - Resource name
        * - :attr:`AMOUNT`
          - :struct:`Scalar`
          - Total amount remaining (only valid while engine is running)
        * - :attr:`CAPACITY`
          - :struct:`Scalar`
          - Total amount when full (only valid while engine is running)
        * - :attr:`DENSITY`
          - :struct:`Scalar`
          - Density of this resource
        * - :attr:`RATIO`
          - :struct:`Scalar`
          - Volumetric flow ratio of this resource


.. attribute:: ConsumedResourceRCS:NAME

    :access: Get only
    :type: :struct:`String`

    The name of the resource, i.e. "LIQUIDFUEL", "ELECTRICCHARGE", "MONOPROP".

.. attribute:: ConsumedResourceRCS:AMOUNT

    :access: Get only
    :type: :struct:`Scalar`

    The value of how much resource is left and accessible to this thruster. Only valid while the thruster is running.

.. attribute:: ConsumedResourceRCS:CAPACITY

    :access: Get only
    :type: :struct:`Scalar`

    What AMOUNT would be if the resource was filled to the top. Only valid while the thruster is running.

.. attribute:: ConsumedResourceRCS:DENSITY

    :access: Get only
    :type: :struct:`Scalar`

    The density value of this resource, expressed in Megagrams f mass
    per Unit of resource.  (i.e. a value of 0.005 would mean that each
    unit of this resource is 5 kilograms.  Megagrams [metric tonnes] is
    the usual unit that most mass in the game is represented in.)

.. attribute:: ConsumedResource:RCSRATIO

    :access: Get only
    :type: :struct:`Scalar`

    What is the volumetric ratio of this fuel as a proportion of the overall fuel mixture, e.g. if this is 0.5 then this fuel is half the required fuel for the thruster.
