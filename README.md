# website
<!DOCTYPE html>
<html>
  <head>
    <title>Possible jQuery Demos Skeleton Page</title>

    <script type="text/javascript" src="//ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>

<!-- Initially hide demo divs and let user know that demo type is undefined -->
    <script type="text/javascript">
      $(document).ready(function() {
        $("#hide_show_div, #events_1_div, #animation_div, #other_feature_div").hide();
        $("#output_checked_radio_val").append("<span>Selected demo type is: undefined</span>" );
      });
    </script>

<!-- Click handling function for all radio buttons in #demo_types_div  -->
    <script type="text/javascript">
      $(document).ready(function() {
        $("#demo_types_div input[name='demo_type']" ).click(function(){
          var demo_type_checked = $("#demo_types_div input[name='demo_type']:checked").val();
          $("#output_checked_radio_val").empty();
          $("#output_checked_radio_val").append("<span>Selected demo type is: " + demo_type_checked + "</span>" );
          $("#empty_div, #hide_show_div, #events_1_div, #animation_div, #other_feature_div").hide();
          switch(demo_type_checked)
          {
            case "hide_show":
              $("#hide_show_div").show();
            break;
            case "events_1":
              $("#events_1_div").show();
            break;
            case "animation":
              $("#animation_div").show();
            break;
            case "other_feature":
              $("#other_feature_div").show();
            break;
          }
        });
      });
    </script>

<!-- Functions for hide_show_div -->
    <script type="text/javascript">
      $(document).ready (function() {
        $('#hide_button').click(function(event) {          
          $("p").hide(); 
        });
        $('#show_button').click(function(event) {
          $("p").show();
        });
        $('#bold_button').click(function(event) {
          $("p").addClass("myEmphasis");
        });
      });  
    </script>
<!-- End of functions for hide_show_div -->

    <style type="text/css">

        body {font-family: Arial, Helvetica, sans-serif; font-size: small;}

        div
        {
          padding-top: 3px; padding-right: 3px; padding-bottom: 3px; padding-left: 3px; 
          margin-top: 3px; margin-right: 3px; margin-bottom: 3px; margin-left: 3px; 
          border-top-color: black; border-right-color: black; border-bottom-color: black; border-left-color: black; 
          border-top-width: thin; border-right-width: thin; border-bottom-width: thin; border-left-width: thin; 
          border-left-style: solid; border-right-style: solid; border-top-style: solid; border-bottom-style: solid;
          -webkit-border-radius: 6px;
          -moz-border-radius: 6px;
          border-radius: 6px;
          -webkit-box-shadow: 2px 2px 10px 0px rgba(0, 0, 0, .3);
          -moz-box-shadow: 2px 2px 10px 0px rgba(0, 0, 0, .3);
          box-shadow: 2px 2px 10px 0px rgba(0, 0, 0, .3);
        }

        #container {margin:auto; width: 600px;}

        #output_checked_radio_val {text-align: center; font-weight: bold;}

        #empty_div, #hide_show_div, #events_1_div, #animation_div, #other_feature_div {height: 300px;}

        .myEmphasis {font-weight: bold;}
    </style>

  </head>

  <body> 
    <div id="container">
      <div id="demo_types_div">
        <table style="width:100%;">
          <tr>
            <td>
              <input id="Radio1" name="demo_type" type="radio" value="hide_show" />Hide / Show</td>
            <td>
              <input id="Radio2" name="demo_type" type="radio" value="events_1" />Events 1</td>
            </tr>
            <tr>
              <td>
                <input id="Radio3" name="demo_type" type="radio" value="animation" />Animation 1</td>
             <td>
               <input id="Radio4" name="demo_type" type="radio" value="other_feature" />Other Feature</td>
           </tr>
        </table>
      </div><!-- end of #demo_types_div -->
    
    <div id="output_checked_radio_val">
    </div><!-- end of #output_checked_radio_val -->

    <div id="empty_div">
      <!--This should appear only when no type has been selected -->   
      <p>Please select a demo type using the radio buttons above</p> 
    </div><!-- end of #empty_div -->
 
    <div id="hide_show_div">
      <!--This should appear only when type is hide_show -->   
      <p>This is paragraph 1.</p>       <p>This is paragraph 2.</p>       <form>         <input type="button" id="hide_button" value="Hide">         <input type="button" id="show_button" value="Show">         <input type="button" id="bold_button" value="Bold">       </form> 
    </div><!-- end of #hide_show_div -->

    <div id="events_1_div">
      <!--This should appear only when type is events_1 -->   
      <p>This is events_1.</p> 
    </div><!-- end of #events_1_div -->

    <div id="animation_div">
      <!--This should appear only when type is animation -->   
      <p>This is animation.</p> 
    </div><!-- end of #animation_div -->

    <div id="other_feature_div">
      <!--This should appear only when type is other_feature -->   
      <p>This is other_feature.</p> 
    </div><!-- end of #other_feature_div -->

  </div><!-- end of #container -->

</body>
</html>
