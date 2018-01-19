---
UID: NF:fwpsk.FwpsReleaseClassifyHandle0
title: FwpsReleaseClassifyHandle0 function
author: windows-driver-content
description: A callout driver calls FwpsReleaseClassifyHandle0 to release a classification handle that was previously acquired through a call to FwpsAcquireClassifyHandle0.Note  FwpsReleaseClassifyHandle0 is a specific version of FwpsReleaseClassifyHandle.
old-location: netvista\fwpsreleaseclassifyhandle0.htm
old-project: netvista
ms.assetid: d61f9e04-e308-4844-9d46-d15faee04e75
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: FwpsReleaseClassifyHandle0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fwpsk.h
req.include-header: Fwpsk.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with  Windows 7.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: FwpsReleaseClassifyHandle0
req.alt-loc: fwpkclnt.lib,fwpkclnt.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Fwpkclnt.lib
req.dll: 
req.irql: <= DISPATCH_LEVEL
req.typenames: FWPS_VSWITCH_EVENT_TYPE
---

# FwpsReleaseClassifyHandle0 function



## -description
A callout driver calls 
  <b>FwpsReleaseClassifyHandle0</b> to release a classification handle that was previously acquired through a
  call to 
  <a href="..\fwpsk\nf-fwpsk-fwpsacquireclassifyhandle0.md">
  FwpsAcquireClassifyHandle0</a>.



## -syntax

````
void NTAPI FwpsReleaseClassifyHandle0(
  _In_ UINT64 classifyHandle
);
````


## -parameters

### -param classifyHandle [in]

The classification handle that identifies the callout driver's processing at the current layer.
     This handle is obtained by calling 
     <a href="..\fwpsk\nf-fwpsk-fwpsacquireclassifyhandle0.md">
     FwpsAcquireClassifyHandle0</a>.


## -returns
None


## -remarks
Any time 
    <a href="..\fwpsk\nf-fwpsk-fwpsacquireclassifyhandle0.md">FwpsAcquireClassifyHandle0</a> is
    called, a corresponding call to 
    <b>FwpsReleaseClassifyHandle0</b> must be made to free the system resources associated with the
    classification handle.


## -see-also
<dl>
<dt>
<a href="..\fwpsk\nc-fwpsk-fwps_callout_classify_fn0.md">classifyFn</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551229">FWPS_CLASSIFY_OUT0</a>
</dt>
<dt>
<a href="..\fwpsk\nf-fwpsk-fwpsacquireclassifyhandle0.md">FwpsAcquireClassifyHandle0</a>
</dt>
<dt>
<a href="..\fwpsk\nf-fwpsk-fwpscompleteclassify0.md">FwpsCompleteClassify0</a>
</dt>
<dt>
<a href="..\fwpsk\nf-fwpsk-fwpspendclassify0.md">FwpsPendClassify0</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20FwpsReleaseClassifyHandle0 function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
