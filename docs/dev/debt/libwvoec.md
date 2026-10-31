# libwvoec technical debt

### Unknown function info

- [77 exports](../../../core/libs/prx/libwvoec/Export.cpp) (libwvoec) - every function export of `libwvoec.sprx` from the firmware 13.60 export table. Signatures, parameter layouts and behaviour are unknown; every export throws through `NotImplemented_nid_no_patch` and keeps the no-parameter import-resolution convention. 72 carry the obfuscated Widevine OEMCrypto entry-point names `_oecc01` to `_oecc110`, `_oecc901` and `_oecc902` whose `tools/nid_names.py` hash equals their NID; a name match does not establish their prototypes. `libwvoecUnknown68` to `libwvoecUnknown72` have no known name and are bound by NID.
