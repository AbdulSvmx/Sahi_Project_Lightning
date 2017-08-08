
/**
 * Function to perform common actions
 */
var $bo_act_common = new function bo_act_common() {

    /**
     * Navigates to Home  page
     * @returns boolean
     */this.navigateToHome = function() {
	_click($bo_pg_home.btn_home);
	_wait(60000, _isVisible($bo_pg_home.link_servicemaxSetup));
	if (_exists($bo_pg_home.link_servicemaxSetup )) {
	    return true;
	} else {
	    return false;
	}
    };

    /**
     * Navigates to Servicemax setup page
     * @returns boolean
     */this.navigateToSvmxSetup = function() {
	this.navigateToHome();
	_click($bo_pg_home.link_servicemaxSetup );
	_wait(3000,_isVisible($bo_pg_servicemaxSetup.btn_serviceFlowManager));
	if (_exists($bo_pg_servicemaxSetup.btn_serviceFlowManager)) {
	    return true;
	} else {
	    return false;
	}
    };
    
    /**
     * Navigates to a SFm transaction designer
     * @returns boolean
     */this.navigateToSfmTransactionDesigner = function() {
	 this.navigateToSvmxSetup();
	_click($bo_pg_servicemaxSetup.btn_serviceFlowManager);
	_click($bo_pg_servicemaxSetup.btn_sfmTransactionAndDocsDesigner);
	_setSpeed(3000);
	if (_exists($bo_pg_sfmTransactionAndDesigner.btn_standardSfmTransaction)) {
	    return true;
	} else {
	    //_log("Exceptions");
	    //Should give control to the test designer to handle the exceptions as hey may need a false positive scenario as well
	    return false;
	}
	
    };

}