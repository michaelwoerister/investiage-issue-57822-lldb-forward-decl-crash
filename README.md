LLDB crashes with forward declaration
=====================================

Q: What does the DWARF data look like? Is it really a forward declaration?

This is the error:
`error: libxul.so DWARF DIE at 0x1d409e77 (class closure) has a member variable 0x1d409e7e (__0) whose type is a forward declaration, not a complete definition.`

```
268785456-    <1d409e47>   DW_AT_type        : <0x1d3fd173>
268785457-    <1d409e4b>   DW_AT_alignment   : 8
268785458-    <1d409e4c>   DW_AT_data_member_location: 0
268785459- <2><1d409e4d>: Abbrev Number: 6 (DW_TAG_member)
268785460-    <1d409e4e>   DW_AT_name        : (indirect string, offset: 0x1ff4ac2): __1
268785461-    <1d409e52>   DW_AT_type        : <0x1d3b6f4f>
268785462-    <1d409e56>   DW_AT_alignment   : 8
268785463-    <1d409e57>   DW_AT_data_member_location: 8
268785464- <2><1d409e58>: Abbrev Number: 0
268785465- <1><1d409e59>: Abbrev Number: 5 (DW_TAG_structure_type)
268785466-    <1d409e5a>   DW_AT_name        : (indirect string, offset: 0x1410805): closure
268785467-    <1d409e5e>   DW_AT_byte_size   : 32
268785468-    <1d409e5f>   DW_AT_alignment   : 8
268785469- <2><1d409e60>: Abbrev Number: 6 (DW_TAG_member)
268785470-    <1d409e61>   DW_AT_name        : (indirect string, offset: 0xabe2486): __0
268785471:    <1d409e65>   DW_AT_type        : <0x1d409e77>
268785472-    <1d409e69>   DW_AT_alignment   : 8
268785473-    <1d409e6a>   DW_AT_data_member_location: 0
268785474- <2><1d409e6b>: Abbrev Number: 6 (DW_TAG_member)
268785475-    <1d409e6c>   DW_AT_name        : (indirect string, offset: 0x1ff4ac2): __1
268785476-    <1d409e70>   DW_AT_type        : <0x1d40508d>
268785477-    <1d409e74>   DW_AT_alignment   : 8
268785478-    <1d409e75>   DW_AT_data_member_location: 24
268785479- <2><1d409e76>: Abbrev Number: 0
268785480: <1><1d409e77>: Abbrev Number: 5 (DW_TAG_structure_type)
268785481-    <1d409e78>   DW_AT_name        : (indirect string, offset: 0x1410805): closure
268785482-    <1d409e7c>   DW_AT_byte_size   : 24
268785483-    <1d409e7d>   DW_AT_alignment   : 8
268785484- <2><1d409e7e>: Abbrev Number: 6 (DW_TAG_member)
268785485-    <1d409e7f>   DW_AT_name        : (indirect string, offset: 0xabe2486): __0
268785486-    <1d409e83>   DW_AT_type        : <0x1d409e8a>
268785487-    <1d409e87>   DW_AT_alignment   : 8
268785488-    <1d409e88>   DW_AT_data_member_location: 0
268785489- <2><1d409e89>: Abbrev Number: 0
268785490- <1><1d409e8a>: Abbrev Number: 5 (DW_TAG_structure_type)
268785491-    <1d409e8b>   DW_AT_name        : (indirect string, offset: 0x1410805): closure
268785492-    <1d409e8f>   DW_AT_byte_size   : 24
268785493-    <1d409e90>   DW_AT_alignment   : 8
268785494- <2><1d409e91>: Abbrev Number: 6 (DW_TAG_member)
268785495-    <1d409e92>   DW_AT_name        : (indirect string, offset: 0xabe2486): __0
```
