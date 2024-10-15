jQuery(window).scroll(function(){
  var sticky = jQuery('header.navbar'),
      backSticky = jQuery('.back_to_ecosystem .fixed-top'),
      scroll = jQuery(window).scrollTop();

  if (scroll >= 100 ){ sticky.addClass('fixed');
        sticky.css("animation", "smoothScroll 3s forwards"); 
    }
  else { sticky.removeClass('fixed');
     sticky.css("animation", "smoothScroll 3s forwards"); 
    }

    if (scroll >= 100 ){ backSticky.addClass('fixed');
        backSticky.css("animation", "smoothScroll 3s forwards"); 
    }
    else { backSticky.removeClass('fixed');
     backSticky.css("animation", "smoothScroll 3s forwards"); 
    }
});


jQuery(document).ready(function() {
    jQuery('ul.nav-sub li a[href^="#"]').bind('click', function(e) {
        e.preventDefault(); // prevent hard jump, the default behavior

        var target = jQuery(this).attr("href"); // Set the target as variable

        // perform animated scrolling by getting top-position of target-element and set it as scroll target
        jQuery('html, body').animate({scrollTop: jQuery(target).offset().top -100 }, 'slow');

        return false;
    });

    var headerHeight = jQuery("header.navbar").height();

    if (jQuery('.back_to_ecosystem').length > 0) {
        var headerHeightFull = headerHeight + 100;
    }else{
        var headerHeightFull = headerHeight + 10;
    }


    // console.log(headerHeightFull);

    jQuery('section.program-detail-tabs-section ul.nav-tabs li a').on('click', function(e) {
        e.preventDefault(); // prevent hard jump, the default behavior
        jQuery('section.program-detail-tabs-section ul.nav-tabs li a').removeClass('active');
        jQuery(this).addClass('active');

        var target = jQuery(this).attr("href"); // Set the target as variable
        var scrollToPosition = jQuery(target).offset().top - headerHeightFull;

        // perform animated scrolling by getting top-position of target-element and set it as scroll target
        jQuery('html, body').stop().animate({ 'scrollTop': scrollToPosition }, 600, function() {
            window.location.hash = "" + target;
            jQuery('html, body').animate({ 'scrollTop': scrollToPosition }, 0);
        });

        return false;
    });


    jQuery('ul.nav-sub li a').on('click', function(e) {
        e.preventDefault(); // prevent hard jump, the default behavior
        jQuery('ul.nav-sub li a').removeClass('active');
        jQuery(this).addClass('active');

        var target = jQuery(this).attr("href"); // Set the target as variable
        var scrollToPosition = jQuery(target).offset().top - headerHeightFull;

        // perform animated scrolling by getting top-position of target-element and set it as scroll target
        jQuery('html, body').stop().animate({ 'scrollTop': scrollToPosition }, 600, function() {
            window.location.hash = "" + target;
            jQuery('html, body').animate({ 'scrollTop': scrollToPosition }, 0);
        });

        return false;
    });


});

jQuery(window).scroll(function() {
    var scrollDistance = jQuery(window).scrollTop();

    // Show/hide menu on scroll
    //if (scrollDistance >= 850) {
    //    jQuery('nav').fadeIn("fast");
    //} else {
    //    jQuery('nav').fadeOut("fast");
    //}
  
    // Assign active class to nav links while scolling
    // jQuery('.section').each(function(i) {
    //     if (jQuery(this).position().top <= scrollDistance) {
    //         jQuery('ul.nav-sub li a.active').removeClass('active');
    //         jQuery('ul.nav-sub li a').eq(i).addClass('active');
    //     }
    // });

    jQuery('.section_scroll').each(function(i) {
        if (jQuery(this).position().top <= scrollDistance) {
            jQuery('ul.nav-tabs li a.active').removeClass('active');
            jQuery('ul.nav-tabs li a').eq(i).addClass('active');
        }
    });


}).scroll();

// function classToggle() {
//   const navs = document.querySelectorAll('.Navbar__Items')
  
//   navs.forEach(nav => nav.classList.toggle('Navbar__ToggleShow'));
// }

// document.querySelector('.Navbar__Link-toggle')
//   .addEventListener('click', classToggle);






( function() {

    var youtube = document.querySelectorAll( ".youtube" );
    
    for (var i = 0; i < youtube.length; i++) {
        
        var source = "https://img.youtube.com/vi/"+ youtube[i].dataset.embed +"/sddefault.jpg";
        
        var image = new Image();
                image.src = source;
                image.addEventListener( "load", function() {
                    youtube[ i ].appendChild( image );
                }( i ) );
        
                youtube[i].addEventListener( "click", function() {

                    var iframe = document.createElement( "iframe" );

                            iframe.setAttribute( "allow", "autoplay" );
                            iframe.setAttribute( "autoplay", "1" );
                            iframe.setAttribute( "frameborder", "0" );
                            iframe.setAttribute( "allowfullscreen", "" );
                            iframe.setAttribute( "src", "https://www.youtube.com/embed/"+ this.dataset.embed +"?rel=0&showinfo=0&autoplay=1" );

                            this.innerHTML = "";
                            this.appendChild( iframe );
                } );    
    };
    
} )();


jQuery(document).ready(function () {
    // Handler for .ready() called.
    var urlHash = window.location.href.split("#")[1];
    jQuery('html, body').animate({
         scrollTop: jQuery('#' + urlHash).offset().top
    }, 'slow');
});


jQuery(document).ready(function () {
    // jQuery(window).on('resize', function(){
    // var ccc = jQuery('.mtsnb').height();
    // var nnn = ccc +32;
    // jQuery("header.navbar.navbar.navbar-light.position-fixed.fixed-top.top_header").css('top', ccc);
    // jQuery(".admin-bar header.navbar.navbar.navbar-light.position-fixed.fixed-top.top_header.aaa.fixed").css('top', nnn);
    // jQuery("header.navbar .navbar-collapse").css('top', ccc);
    // });

    jQuery("a.mtsnb-hide").click(function(){
      jQuery("body").removeClass("has-mtsnb");
    });
});



jQuery(window).on('resize', function(){
//jQuery(document).ready(function() {
  jQuery(".video_info video").css("height", jQuery(".body.collections ul.products.columns-3 li.product .pro-thumb img").height());
});