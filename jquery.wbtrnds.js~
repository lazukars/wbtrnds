
	var wt = {
		settings : {
		},
			
		init : {
			extendOptions : function(el, options){
				if(options){
					wt.settings = $.extend(wt.settings, options);
				}
			},	
			build : function(el){
				if(el){
					el.each( function(){
						$(this)
							.click(function(){
								// The selected class name must be the LAST class of an element for this to work 
								var className = $(this).attr('class').split(' ').slice(-1);
								dcsMultiTrack('DCS.dcsuri', wt.settings[className].url, 'WT.ti' , wt.settings[className].name);
							});
					});
				}else{ return false }
			}
		}
	}


	if (typeof Object.create !== 'function') {
		Object.create = function (o) {
			function F() {}
			F.prototype = o;
			return new F();
	   	};
	}

	(function($) {

		$.fn.wbtrnds = function(options) {
			this.each(function() {
				var myWebtrends = Object.create(wt);
				for( prop in myWebtrends.init ){
					myWebtrends.init[prop]($(this), options);
				}
			});
			return this;
		};

	})(jQuery);

