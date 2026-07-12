# encapsulation-smart-door-system

#A Smart Door Access System For UMaT

This repo contains a python notebook that contains codes used to develop a smart door access system for UMaT admin staff with each staff having an access code that must be protected from direct modification.

#Key Breakdown of Encapsulation Used:

Private Attribute (__access_code): The double underscore triggers Python's name mangling, which prevents outside code from directly modifying or reading staff1.__access_code.

The @property Decorator (Getter): This turns a method into a read-only property. When you call staff1.access_code, it executes the function logic (where we can intercept and check for authorization) rather than giving raw data access.

The @access_code.setter: This interceptor validates any data before it gets saved to the private variable. If the rules aren't met (like the 6-character length rule), it rejects the change.
