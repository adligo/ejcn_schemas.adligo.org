# EJCN Schemas

### Abstract

This project is devoted to EJCN schemas, which enable you to provide a [UML](#uml) style package and class name structure to describe EJCN data.  

# Naming & Name Space

Throughout the history of programming and computer science, naming has been a hot topic.

For EJCN Schemas, we suggest the use of [snake case](#snake-case) for package names and <b>English Proper Noun</b> style capitalization (first letter) for class names, with subsequent letters following the [camel case](#camel-case) convention.

In addition, we suggest all name parts stay less than 63 characters.

- [Excerpt from DNS Host Names rfc1035](#dns)
```
The labels must follow the rules for ARPANET host names.  They must
start with a letter, end with a letter or digit, and have as interior
characters only letters, digits, and hyphen.  There are also some
restrictions on the length.  Labels must be 63 characters or less.
```

# Class Names 

Here the word [class](#uml-classes) is synonymous with the [UML definition](#uml-classes).  However, more specifically, all EJCN Classes are extensions of a specific kind of class, which represents EJCN data.  This special class has the following fully qualified EJCN Schema name.

### not_dns.ejcn.Class

Therefore, all EJCN classes must extend from <b>not_dns.ejcn.Class</b>.

# Package Names

Package names are comprised of sub-domains nearly identical to [DNS](#dns).  However, similar to Java and LDAP name spaces, the top-level domain exists at the left and moves to the smallest sub-domain, which is at the right.  In addition, we introduce this special <b>not_dns</b> top-level domain.

##### The not_dns. Top Level Domain

The <b>not_dns</b> top level domain allows usage of this system, for code bases which have decided not to use DNS or register a corresponding DNS name.  However, users of not-DNS are encouraged to append to this specification requesting a specific non-DNS name.  For example; <b>'not_dns.namecoin.example'</b>

# Fully Qualified Class Loader Name-Space Names

EJCN serializers and parser will have an optional class loader similar to [Java's Class Loader](#java).  


### Serializers

EJCN serializers are used to write EJCN data to files and socket streams.  Serializers MAY optionally validate data when they write it out from memory.  Validation when writing data has often been called marshaling.

### Parsers

EJCN parsers are used to read EJCN data in from files and socket streams.  Serializers MAY optionally validate data when they read it in to memory.  Validation when writing data has often been called un-marshaling.

# Regular Expressions

EJCN will allow for usage of ECMA Script regular expressions to validate data during.  Most major languages will support this indirectly, ECMAScript clearly supports it natively.  In addition, there are runtime ECMA Script implementations which can be embedded into most major programming platforms, including Java's JVM (Closure, Kotlin, Groovy, Scala, Unicorn, etc), C#, Go, Python, and Rust.

# Commentary

This work was partially inspired by JSON Schemas, JSON Lines, Smithy, Java Serialization, XML, JSON itself, and many other tools and frameworks attempting to achieve the same goals.  Everyone would like a standard for data interchange, however, various forces have caused these standards to come in and out of fashion over the years.  This schema specification attempts to be a standard of standards, allowing the incorporation of anything anyone else could come up with.

# Citations


### ARPA Text Messages

- [STANDARD FOR THE FORMAT OF ARPA INTERNET TEXT MESSAGES rfc822 ](https://datatracker.ietf.org/doc/html/rfc822)

### Camel Case

 - [Wikipedia](https://en.wikipedia.org/wiki/Camel_case)

### DNS

- [DOMAIN NAMES - IMPLEMENTATION AND SPECIFICATION rfc1035](https://datatracker.ietf.org/doc/html/rfc1035)
- [Host Names rfc1035](https://datatracker.ietf.org/doc/html/rfc1035#section-2.3.1)
- [Wikipedia Top Level Domains](https://en.wikipedia.org/wiki/List_of_Internet_top-level_domains)

### James Gosling

- [James Gosling JVM Languages Summit 2024](https://youtu.be/zg8xM0xxFa8)

### Java

- [Java Naming Conventions](https://www.oracle.com/java/technologies/javase/codeconventions-namingconventions.html)

### JNDI

- [Sun's JNDI Book](references/JNDI_Sun.pdf)

### Naming Convention Opinions

- [On the Naming of Methods: A Survey of Professional Developers](references/DevsOnNaming.pdf)

### Snake Case

- [Wikipedia](https://en.wikipedia.org/wiki/Snake_case)

### UML

* [Unified Modeling Language (UML) 2.5.1](https://www.omg.org/spec/UML/2.5.1/)
* [UML-Diagrams.org](https://www.uml-diagrams.org/) - Comprehensive reference for all diagram types.
* [Lucidchart UML Guide](https://www.lucidchart.com/pages/uml-diagram-types) - Beginner-friendly explanations.
* [Mermaid.js Documentation](https://mermaid.js.org/intro/) - The syntax used for the diagrams in this README.

### UML Classes

- [IBM](https://www.ibm.com/docs/en/dma?topic=diagrams-classes)
- [Visual Paradigm](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-class-diagram-tutorial/)
- [Wikipedia](https://en.wikipedia.org/wiki/Class_diagram)
- [Uml-Diagrams.org](https://www.uml-diagrams.org/class.html)
