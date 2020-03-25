<script>
  import Vizceral from "vizceral-svelte";
  import traffic from "./sample_data.json";
  let styles = {
    colorText: "rgb(214, 214, 214)",
    colorTextDisabled: "rgb(129, 129, 129)",
    colorTraffic: {
      normal: "rgb(186, 213, 237)",
      normalDonut: "rgb(91, 91, 91)",
      warning: "rgb(268, 185, 73)",
      danger: "rgb(184, 36, 36)"
    },
    colorNormalDimmed: "rgb(101, 117, 128)",
    colorBackgroundDark: "rgb(35, 35, 35)",
    colorLabelBorder: "rgb(16, 17, 18)",
    colorLabelText: "rgb(0, 0, 0)",
    colorDonutInternalColor: "rgb(35, 35, 35)",
    colorDonutInternalColorHighlighted: "rgb(255, 255, 255)",
    colorConnectionLine: "rgb(91, 91, 91)",
    colorPageBackground: "rgb(45, 45, 45)",
    colorPageBackgroundTransparent: "rgba(45, 45, 45, 0)",
    colorBorderLines: "rgb(137, 137, 137)",
    colorArcBackground: "rgb(60, 60, 60)"
  };
</script>

<Vizceral {styles} {traffic} />
