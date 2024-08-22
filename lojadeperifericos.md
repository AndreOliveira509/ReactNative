import React from 'react';
import { StyleSheet, Text, View, FlatList, Image } from 'react-native';
const App = () => {
 const data = [
 { id: '1', title: 'Teclado Mecânico Gamer HyperX Alloy Origins 60%, RGB, USB, HyperX Red Switch', text: 'R$ 505,99', img: 'https://www.kabum.com.br/_next/image?url=https%3A%2F%2Fimages.kabum.com.br%2Fprodutos%2Ffotos%2F150980%2Fteclado-mecanico-gamer-hyperx-alloy-origins-60-rgb-usb-hyperx-red-switch-design-compacto-anti-ghosting-abnt2-preto-hkbo1s-rb-usg_1616771985_m.jpg&w=256&q=75' },
 { id: '2', title: 'Headset Gamer Razer Kraken X Lite, Surround 7.1, Drivers 40mm, P2', text: 'R$ 145,99', img: 'https://www.kabum.com.br/_next/image?url=https%3A%2F%2Fimages.kabum.com.br%2Fprodutos%2Ffotos%2F104667%2Fheadset-gamer-razer-kraken-x-lite-p2_headset-gamer-razer-kraken-x-lite-p2_1569864643_m.jpg&w=256&q=75' },
 { id: '3', title: 'Mouse Gamer Redragon King Cobra Chroma RGB, 24000 DPI', text: 'R$ 211,99', img: 'https://www.kabum.com.br/_next/image?url=https%3A%2F%2Fimages.kabum.com.br%2Fprodutos%2Ffotos%2Fsync_mirakl%2F156665%2FMouse-Gamer-Redragon-King-Cobra-Chroma-RGB-24000-DPI-Switch-a-Laser-Sensor-Pixart-3360-M711-FPS_1713371297_m.jpg&w=256&q=75' },
 { id: '4', title: 'Mouse Gamer Logitech G403 HERO com RGB LIGHTSYNC, 6 Botões Programáveis', text: 'R$ 229,90', img: 'https://www.kabum.com.br/_next/image?url=https%3A%2F%2Fimages.kabum.com.br%2Fprodutos%2Ffotos%2F102649%2Fmouse-gamer-logitech-g403-hero-com-rgb-lightsync-6-botoes-programaveis-ajuste-de-peso-e-sensor-hero-25k-910-005631_1700850718_m.jpg&w=256&q=75' },
 { id: '5', title: 'Monitor Gamer Curvo LG UltraGear LG 34", UltraWide, 160Hz, WQHD, 1ms' , text: 'R$ 2.059,99', img: 'https://www.kabum.com.br/_next/image?url=https%3A%2F%2Fimages.kabum.com.br%2Fprodutos%2Ffotos%2F472908%2Fmonitor-gamer-lg-ultragear-lg-34-curvo-led-wqhd-ultrawide-160hz-1ms-displayport-e-hdmi-amd-freesync-premium-hdr10-99-srgb-34gp63a-b_1717591886_m.jpg&w=256&q=75' },
  { id: '6', title: 'Monitor Gamer Samsung Odyssey G5 34” Uwqhd, Tela Curva Ultrawide' , text: 'R$ 3.159,00', img: 'https://www.kabum.com.br/_next/image?url=https%3A%2F%2Fimages.kabum.com.br%2Fprodutos%2Ffotos%2Fsync_mirakl%2F602367%2FMonitor-Gamer-Samsung-Odyssey-G5-34-Uwqhd-Tela-Curva-Ultrawide-Painel-Va-165hz-1ms-Hdr10-HDMI-Dp-Freesync-Premium-Preto_1723665737_m.jpg&w=256&q=75' },
   { id: '7', title: 'Headset Gamer Sem Fio Corsair HS55, 7.1 Surround, Driver 50mm, Wireless, Branco' , text: 'R$ 339,99', img: 'https://www.kabum.com.br/_next/image?url=https%3A%2F%2Fimages2.kabum.com.br%2Fprodutos%2Ffotos%2F570322%2Fheadset-gamer-sem-fio-corsair-hs55-7-1-surround-driver-50mm-wireless-branco-ca-9011281-na_1718371411_m.jpg&w=256&q=75' },
    { id: '8', title: 'Teclado Mecânico GAMING TG600, Preto, 60% e ABNT2, RGB, Switch Gateron Red ' , text: 'R$ 209,99', img: 'https://www.kabum.com.br/_next/image?url=https%3A%2F%2Fimages6.kabum.com.br%2Fprodutos%2Ffotos%2F472046%2Fteclado-mecanico-gamer-kbm-gaming-tg600-preto-60-e-abnt2-rgb-switch-gateron-red-kgtg600ptvr_1717444896_m.jpg&w=256&q=75' },
     { id: '9', title: 'Fone de Ouvido Sem fio HyperX Cloud MIX Buds, Bluetooth' , text: 'R$ 459,00', img: 'https://www.kabum.com.br/_next/image?url=https%3A%2F%2Fimages.kabum.com.br%2Fprodutos%2Ffotos%2F444751%2Ffone-de-ouvido-sem-fio-hyperx-cloud-mix-buds-bluetooth-compativel-com-pc-ps5-ps4-nintendo-switch-celular-preto-4p5d9aa_1681328121_m.jpg&w=256&q=75' },
      { id: '10', title: 'Microfone Gamer HyperX QuadCast S Podcast, Antivibração, LED RGB, USB' , text: 'R$ 729,90', img: 'https://www.kabum.com.br/_next/image?url=https%3A%2F%2Fimages.kabum.com.br%2Fprodutos%2Ffotos%2F117767%2Fmicrofone-gamer-hyperx-quadcast-s-led-usb-preto-e-vermelho-hmiq1s-xx-rg-g_1602169935_m.jpg&w=256&q=75' }
 ];
 return (
 <View style={styles.container}>
    <Text style={styles.title}>Perifericos</Text>
  <FlatList
    data={data}
    keyExtractor={(item) => item.id}
    renderItem={({ item }) => (
 <View style={styles.item}>
  <Image source={{ uri: item.img }} style={styles.img}/>
 <View style={styles.boxflex}>
  <Text style={styles.itemText}>{item.title}</Text>
  <Text style={styles.itemTextp}>{item.text}</Text>
  </View>
 </View>
 )}
 />
 </View>
 );
};
const styles = StyleSheet.create({
 container: {
 flex: 1,
 backgroundColor: '#ddd',
 paddingTop: 30,
 
 },
 title: {
 fontSize: 24,
 fontWeight: 'bold',
 textAlign: 'center',
 marginBottom: 20,
 color: '#000'
 },
 boxflex:{
    flex: 1,
    marginLeft: 10,
 },
 itemTextp:{
   color: '#0000FF',
   textDecorationLine: 'underline',
 },
 img: {
   borderRadius: 5,
   width: 80,
   height: 80,
   
 },
 item: {
 height: 150,
 flexDirection: 'row',
 alignItems: 'center',
 backgroundColor: '#FFF',
 shadowColor: '#171717',
 shadowOffset: {width: -2, height: 4},
 shadowOpacity: 0.2,
 shadowRadius: 3,
 padding: 20,
 borderRadius: 10,
 marginVertical: 8,
 marginHorizontal: 16,
 },
 itemText: {
 fontSize: 16,
  color: '#000'
 },
});
export default App;