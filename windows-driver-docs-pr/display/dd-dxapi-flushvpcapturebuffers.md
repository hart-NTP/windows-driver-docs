---
title: DD_DXAPI_FLUSHVPCAPTUREBUFFERS Control Code (Windows Drivers)
description: Learn more about the DD_DXAPI_FLUSHVPCAPTUREBUFFERS control code.
keywords:
- DD_DXAPI_FLUSHVPCAPTUREBUFFERS
- ddkmapi/DD_DXAPI_FLUSHVPCAPTUREBUFFERS
ms.date: 10/12/2022
---

# DD\_DXAPI\_FLUSHVPCAPTUREBUFFERS control code

A video capture driver passes DD\_DXAPI\_FLUSHVPCAPTUREBUFFERS in the *dwFunctionNum* parameter of the [**DxApi**](nf-dxapi-dxapi.md) function to remove all buffers from the capture queue and to stop video capture for the device.

## Input Parameters

- *lpvInBuffer*  
    Pointer to the VPE capture handle (HANDLE hCapture;).

## Output Parameters

- *lpvOutBuffer*  
    Pointer to a DWORD that contains the DirectDraw return value.

## Remarks

All KEVENTs that have been registered using the [**DD\_DXAPI\_ADDVPCAPTUREBUFFER**](dd-dxapi-addvpcapturebuffer.md) function identifier will be set.

This function identifier can be called at raised IRQL.

## Requirements

Header file: *Ddkmapi.h* (include *Ddkmapi.h*)

## See also

[**DD\_DXAPI\_ADDVPCAPTUREBUFFER**](dd-dxapi-addvpcapturebuffer.md)
