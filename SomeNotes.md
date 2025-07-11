Some Notes:

// Fix Casting: https://github.com/arichornlover/uYouEnhanced/issues/606#issuecomment-2098289942
%group gFixCasting
%hook YTColdConfig
- (BOOL)cxClientEnableIosLocalNetworkPermissionReliabilityFixes { return YES; }
- (BOOL)cxClientEnableIosLocalNetworkPermissionUsingSockets { return NO; }
- (BOOL)cxClientEnableIosLocalNetworkPermissionWifiFixes { return YES; }
%end
%hook YTHotConfig
- (BOOL)isPromptForLocalNetworkPermissionsEnabled { return YES; }
%end
%end
