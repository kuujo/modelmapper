# 0.6.5
4/15/2014

* Fixed #100 - Problem mapping nested collections

# 0.6.4
3/31/2014

* Fixed #95 - Empower ConditionalConverters to handle null properties in source objects
* Fixed #96 - Inherited shaded paths preventing customer converters from running

# 0.6.3 
1/24/2014

* Fixed #80 - ModelMapper extensions use maven backward dependencies
* Fixed #83 - Add MappingContext.create(CS source, CD destination)
* Fixed #82 - Ignore enums when traversing Enum types
* Fixed #85 - Allow non-void setter return types
* FIxed #91 - Add shaded cglib to Export-Package for better OSGi-support

# 0.6.2 
11/5/2013

* Added support for mapping Groovy properties
* Improved jOOQ support
* Fixed #74 - Null intermdiate values possible when instance requested via global provider

# 0.6.0 
8/2/2013

* Added ValueReaders to SPI
* Added 3rd party integration for Jackson, Gson and jOOQ
* Added Simpler mapper EDSL for dealing with providers
* Fixed #8 - Introduced global property conditions
* Fixed #39 - Issue when mapping to a String
* Fixed #49 - Allow implicit mapping to be skipped globally
* Fixed #54 - Fixed OSGI support
* Fixed #56 - Allow full type matching to be required
* Fixed #61 -* Added UNDERSCORE NameTokenizer
* Fixed issue with Javabeans name transformers for get/set methods
* Fixed issue with merged TypeMap Providers not being copied

### API Changes:

* Configuration.enableFieldMatching(boolean) is now setFieldMatchingEnabled(boolean)
* Configuration.ignoreAmbiguity(boolean) is now setAmbiguityIgnored(boolean)

# 0.5.6 
3/21/2013

* Fixed #46 - Property map difficult to construct types
* Added #45 - Android compatibility
* Added #42 - Support for pre and post mapping Converters
* Added #40 - Enhance TypeTokens support
* Fixed #31 - Multiple source properties hierarchy matching problem
* FIxed #38 - Map mocked objects
* Added #34 - Added support for TypeTokens

# 0.5.5 
2/14/2013

* Added support for TypeTokens
* Fixed GH #23 - Support for combined token matching
* Fixed GH #32 - Mapping creates instances for null objects
* Fixed GH #37 - Mappings being incorrectly created

# 0.5.4 
12/22/2012

* Fixed GH #18 - Updated manifest.mf to contain OSGI bundle information for shaded packages
* Fixed GH #26 - MM attempts to instantiate primitive wrapper when used in destination Converter
* Fixed GH #27 - Destinations values are not set in MappingContext
* Fixed GH #30 - Cannot proxy types without a default constructor

# 0.5.3 
10/22/2012

* Fixed GH #22 - Destination properties being cached by mutator
* Fixed GH #21 - Added support for XMLGregorianCalendar conversion
* Fixed issue when merging from a TypeMap with a Converter

# 0.5.2 
10/18/2012

* Fixed GH #19 - Merged mappings should respect MatchingStrategy
* Fixed GH #20 - Enum conversion should support String->Enum

# 0.5.1 
9/26/2012

* Fixed scenario where a circular mapping can overrides an existing mapping
* Fixed GH #11 - Improper shading
* Fixed GH #10 - Added support for mapped enum conversion

# 0.5.0 
9/12/2012

* Fixed GH #2 - Add support for circular references
* Fixed GH #9 - Overriding intemediate objects in provided destinations
* Fixed conversion of char[] to String
* Fixed GC #20 - Improved hashCode in TypeInfoRegistry
* Completed GC #21 - Implement strict matching strategy
* Fixed GC #22 - PropertyMap doesn't work when token matches exist

# 0.4.0 
7/22/2012

* Added support for TypeMap-wide property conditions, converters and providers
* Improved generic type resolution
* Added support for auto-TypeMap merging
* Fixed GH #3: Disambiguation enhancements
* Fixed GH #4: Added source to ProvisionRequest
* Fixed GH #5: Incorrect shading of null paramters
* Fixed GH #7: Conversion skipped when source is null
* Fixed GC #8: Skipped circular properties
* Fixed GC #10: Incorrect mappings created for multiple source mappings

# 0.3.5 
8/8/2011

* Fixed GC #9: Compatibility with Java 5

# 0.3.4 
7/30/2011

* Simplified the ConditionalConverter SPI
* Fixed GC #4: Exposed conditional converters for mutation via Configuration.getConverters()
* Fixed GC #5: Copy null values for primitives

# 0.3.3 
7/26/2011

* Fixed GC #3: Missing repackaged cglib dependencies
* Fixed GC #2: UnsupportedOperationException when adding ConditionalConverters to configuration

# 0.3.2 
7/19/2011

* Rolled back class file target version to 1.5

# 0.3.1 
6/27/2011

* Added better handling of inherited generic component types
* Added support for shaded properties when using a converter, a skipped mapping or a null source constant

# 0.3.0 
6/20/2011

* Initial public release