# FHIR Primer - Implementer Examples

Check the wiki page [here](https://github.com/chrisgrenz/FHIR-Primer/wiki).

## Profiles

### Hierarchy for complete profile
* **patient-extensions** - Adds type profiles for extension elements (no further slicing)
* **patient-name-slice** - Slice Patient.name by a single fixed value
* **patient-telecom-slice** - Slice Patient.telecom by multiple discriminators
* **patient-deceasedDatetime-slice** - Use a type named slicing (deceasedDatetime) of deceased[x].
* **patient-careprovider-type-slice** - Slice a reference by type.
* **patient-careprovider-type-reslice** - Re-slice a reference type slice. 
* **patient-identifier-profile-slice** - slice Patient.identifier using type profiles
* **patient-identifier-slice-extension** - add an extension to one slice of identifier
* **patient-research-auth-reslice** - Re-slice the researchAuth extesion by the value of an extension.  Add an extension to one slice.


### Special Case Profiles
* **patient-deceasedX-slice** - Slice Patient.deceased[x] by @type.
* **patient-telecom-reslice** - Slice telecom in two steps (system, then re-slice by use).
* **patient-gender** - profile with all elements removed _except_ gender.
* **patient-only-mrn** - profile where only the mrn type is allowed.
* **patient-only-mrn-slice** - profile with all elements removed _except_ one slice of identifer (mrn). Closed slicing.