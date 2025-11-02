<Container>
  <Name>Kaspa Node</Name>
  <Repository>kaspanet/rusty-kaspad:latest</Repository>
  <Network>bridge</Network>
  <Privileged>false</Privileged>
  <Support>https://github.com/<yourusername>/unraid-templates</Support>
  <Project>https://github.com/kaspanet/rusty-kaspa</Project>
  <Overview>Official Rust implementation of the Kaspa Node. Fully tested on Unraid 6.12+.</Overview>
  <Category>Blockchain:Node</Category>
  <ExtraParams>--utxoindex --disable-upnp --maxinpeers=64 --outpeers=32 --yes</ExtraParams>
  <Data>
    <Volume>
      <HostDir>/mnt/user/appdata/kaspa</HostDir>
      <ContainerDir>/app/data</ContainerDir>
      <Mode>rw</Mode>
    </Volume>
  </Data>
  <Ports>
    <Port><HostPort>16110</HostPort><ContainerPort>16110</ContainerPort><Protocol>tcp</Protocol></Port>
    <Port><HostPort>16111</HostPort><ContainerPort>16111</ContainerPort><Protocol>tcp</Protocol></Port>
    <Port><HostPort>17110</HostPort><ContainerPort>17110</ContainerPort><Protocol>tcp</Protocol></Port>
  </Ports>
</Container>
